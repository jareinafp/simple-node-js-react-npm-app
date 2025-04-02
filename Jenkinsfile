pipeline {
    agent {
        docker {
            image 'node:16-alpine' // Usa una imagen Docker con Node.js
            //args '-p 3000:3000' //puertos
        }
    }
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/jareinafp/simple-node-js-react-npm-app'
            }
        }
        stage('Instalar dependencias') {
            steps {
                sh 'npm install'
            }
        }
        stage('Construir la aplicación') {
            steps {
                sh 'npm run build' // Asume que tienes un script "build" en package.json
            }
        }
        stage('Desplegar') {
            steps {
                // Aquí, reemplaza con el comando de despliegue específico para tu entorno
                sh 'echo "Desplegando la aplicación..."'
                //Ejemplos:
                //sh 'scp -r build/* usuario@servidor:/ruta/destino/' //despliegue mediante scp.
                //sh 'aws s3 sync build/ s3://mi-bucket-s3' //despliegue en AWS S3.
            }
        }
    }
    post {
        always {
            echo 'Pipeline finalizado'
        }
        success {
            echo 'Despliegue exitoso'
        }
        failure {
            echo 'Despliegue fallido'
        }
    }
}
