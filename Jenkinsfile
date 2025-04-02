pipeline {
agent {
docker {
image 'node:20.10.0-alpine3.18' // Imagen de Docker
args '-p 3001:3001' // Puertos
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
