pipeline {
    agent any

    stages {

        stage('Clonar Repositorio') {
            steps {
                echo 'Descargando el código desde GitHub...'
            }
        }

        stage('Verificar Archivos') {  //ejecuta ls -la para mostrar los archivos del proyecto
            steps {
                sh 'ls -la'
            }
        }

        stage('Mostrar index.html') {   //imprime el contenido de index.html.
            steps {
                sh 'cat index.html'
            }
        }

        stage('Finalizar') {
            steps {
                echo 'Pipeline ejecutado correctamente.'
            }
        }

    }
}