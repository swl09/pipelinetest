node {
    echo 'Hello from Pipeline'
}

node {
    /* ... */
    stage 'Build Docker image'
    def image = docker.build('swilly09/swltest', '.')
}

