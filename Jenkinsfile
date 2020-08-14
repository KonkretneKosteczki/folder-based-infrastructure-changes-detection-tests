pipeline {
    agent any
    stages {
        stage('A folder changes') {
            when {
                changeset pattern: "A/**"
            }
            steps {
                echo 'Deploying A'
            }
        }
        stage('B folder changes') {
            when {
                changeset pattern: "B/**"
            }
            steps {
                echo 'Deploying B'
            }
        }
        stage('A or B folder changes') {
            when {
                anyOf {
                    changeset pattern: "A/**"
                    changeset pattern: "B/**"
                }
            }
            steps {
                echo 'Deploying A or B'
            }
        }
        stage('A and B folder changes') {
            when {
                allOf {
                    changeset pattern: "A/**"
                    changeset pattern: "B/**"
                }
            }
            steps {
                echo 'Deploying A and B'
            }
        }
    }
}
