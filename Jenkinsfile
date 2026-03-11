pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo 'Construyendo proyecto...'
                sh 'echo "Este es mi primer reporte generado por Jenkins" > reporte.txt'
                sh 'zip archivo_comprimido.zip reporte.txt'
            }
        }

        stage('Test') {
            steps {
                echo 'Ejecutando pruebas...'
                sh 'ls -la'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Simulando despliegue...'
                archiveArtifacts artifacts: 'reporte.txt, archivo_comprimido.zip', fingerprint: true
            }
        }

    }
}