pipeline {
    agent any
    stages {
        stage('A trigger') {
            when {
                branch 'master'
                changeset pattern: "A/**", caseSensitive: true
            }
            steps {
                echo 'Deploying A'
            }
        }
        stage('B trigger') {
            when {
                branch 'master'
                changeset pattern: "B/**", caseSensitive: true
            }
            steps {
                echo 'Deploying B'
            }
        }
    }
}
