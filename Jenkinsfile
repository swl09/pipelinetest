node {
    echo 'Hello from Pipeline'
}

node {
    /* ... */
    git 'https://github.com/swl09/pipelinetest.git'
    stage 'Build Docker image'
    def image = docker.build('swilly09/swltest', '.')

    /* ... */
    stage 'Push image'
    docker.withRegistry("https://registry.hub.docker.com", "docker-hub") {
        image.push()
    }
}


