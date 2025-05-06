pipeline {
    agent any

    stages {
        stage('Clonar repositorio') {
            steps {
                git credentialsId: 'mis-credenciales-git', url: 'https://github.com/miusuario/mi-repo.git', branch: 'main'
            }
        }

        stage('Compilar') {
            steps {
                echo 'Compilando el proyecto...'
                // Aquí pondrías el comando real, como: mvn clean install
            }
        }

        stage('Analizar con SonarQube') {
            steps {
                echo 'Análisis estático con SonarQube...'
                // Aquí pondrías por ejemplo: mvn sonar:sonar
            }
        }

        stage('Construir imagen Docker') {
            steps {
                echo 'Construyendo imagen Docker...'
                // docker build -t mi-imagen:1.0 .
            }
        }

        stage('Subir artefacto a Nexus') {
            steps {
                echo 'Subiendo a Nexus...'
                // subir el .jar o .zip a Nexus
            }
        }
    }
}
