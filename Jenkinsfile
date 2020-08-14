pipeline {
    agent any
    stages {
        stage('AB trigger') {
            when {
                branch 'master'
            }
            steps {
                echo 'Deploying AB'
            }
        }
        stage('A trigger') {
            when {
                branch 'master'
                changeset pattern: "/A/**"
            }
            steps {
                echo 'Deploying A'
            }
        }
        stage('B trigger') {
            when {
                branch 'master'
                changeset pattern: "/B/**"
            }
            steps {
                echo 'Deploying B'
            }
        }
    }
}
