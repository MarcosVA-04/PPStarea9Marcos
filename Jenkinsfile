pipeline {
    agent any
    stages {
        stage('Preparación (Build)') {
            steps {
                echo '--- Iniciando Construcción ---'
                sh 'python3 -m venv venv'
                sh './venv/bin/pip install -r requirements.txt'
            }
        }
        stage('Testear (Test)') {
            steps {
                echo '--- Ejecutando Pruebas Unitarias ---'
                sh './venv/bin/pytest'
            }
        }
        stage('Desplegar (Deploy)') {
            steps {
                echo '--- Simulando Despliegue a Producción ---'
                sh 'echo "Despliegue exitoso el $(date)" > resultado_despliegue.txt'
            }
        }
    }
}
