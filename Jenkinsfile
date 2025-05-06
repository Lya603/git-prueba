pipeline {
    agent any

    stages {
        stage('Compilar') {
            steps {
                echo 'Compilando el proyecto...'
                sh './mvnw clean install'
            }
        }

        stage('Test') {
            steps {
                echo 'Ejecutando tests...'
                sh './mvnw test'
            }
        }

        stage('Analizar con SonarQube') {
            steps {
                echo 'Análisis estático con SonarQube...'
                // sh 'mvn sonar:sonar'  // Asegúrate de tener SonarQube configurado
            }
        }

        stage('Construir imagen Docker') {
            steps {
                echo 'Construyendo imagen Docker...'
                // sh 'docker build -t mi-imagen:1.0 .'
            }
        }

        stage('Subir artefacto a Nexus') {
            steps {
                echo 'Subiendo artefacto a Nexus...'
                // sh 'mvn deploy'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Desplegando el proyecto...'
                // Aquí podrías ejecutar comandos de despliegue
            }
        }
    }
}
