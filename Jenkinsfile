node {
    echo 'Hello from Pipeline'
}

node {
    /* ... */
    git 'https://github.com/swl09/pipelinetest.git'
    stage 'Build Docker image'
    def image = docker.build('swilly09/swltest', '.')
}

node {
    /* ... */
    stage 'Push image'
    docker.withRegistry("https://registry.hub.docker.com", "a7a6d5f1-add2-4db4-9326-de3e6d054e8a") {
        image.push()
    }
}


