pipeline {
agent {
docker {
image 'node:20.10.0-alpine3.18' // Imagen de Docker

}
}
stages {
stage('Build') {
steps {
sh 'npm install' // Instalar dependencias
}
}
}
}
