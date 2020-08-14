pipeline {
    agent any
    stages {
        stage('/B trigger') {
            when {
                changeset pattern: "/B/**"
            }
            steps {
                echo 'Deploying B'
            }
        }
        stage('B trigger') {
            when {
                changeset pattern: "B/**"
            }
            steps {
                echo 'Deploying B'
            }
        }
    }
}
