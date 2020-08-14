pipeline {
    agent any
    stages {
        stage('AB trigger') {
            when {
                changeset pattern: "/{A,B}/**"
            }
            steps {
                echo 'Deploying AB'
            }
        }
        stage('A trigger') {
            when {
                changeset pattern: "/A/**"
            }
            steps {
                echo 'Deploying A'
            }
        }
        stage('B trigger') {
            when {
                changeset pattern: "/B/**"
            }
            steps {
                echo 'Deploying B'
            }
        }
    }
}
