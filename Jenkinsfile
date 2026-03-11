pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Fase 1: Construyendo el reporte...'
                // Creamos el archivo de texto
                sh 'echo "Reporte generado por Jenkins el $(date)" > reporte.txt'
                // Usamos tar (que sí está instalado) para comprimir
                sh 'tar -cvf archivo_comprimido.tar reporte.txt'
            }
        }

        stage('Test') {
            steps {
                echo 'Fase 2: Verificando archivos...'
                // Listamos para confirmar que existen
                sh 'ls -la'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Fase 3: Guardando artefactos para descargar...'
                // Esto hace que los archivos aparezcan en la interfaz de Jenkins
                archiveArtifacts artifacts: 'reporte.txt, *.tar', fingerprint: true
            }
        }
    }
}