pipeline {
    agent any
    stages {
        stage('B trigger') {
            when {
                anyOf {
                    changeset pattern: "/B/**"
                    changeset pattern: "B/**"
                    changeset pattern: "**"
                }
            }
            steps {
                echo 'Deploying B'
            }
        }
    }
}
