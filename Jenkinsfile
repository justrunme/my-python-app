pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    // Сборка Docker-образа
                    def app = docker.build("my-python-app")
                }
            }
        }
        stage('Deploy') {
            steps {
                script {
                    // Запуск контейнера на сервере
                    app.run("-d -p 8080:8080")
                }
            }
        }
    }
}
