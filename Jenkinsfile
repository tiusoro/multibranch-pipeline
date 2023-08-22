pipeline {
    agent any
    stages {
        stage("test") {
            steps {
                script {
                    echo "building the application..."
                    echo "Executing pipeline for branch $BRANCH_NAME"
                }
            }
        }
        stage("build") {
            when {
                expression {
                    BRANCH_NAME == 'dev'
                }
            }
            steps {
                script {
                    echo "building the docker image..."
                }
            }
        }
        stage("deploy") {
            when {
                expression {
                    BRANCH_NAME == 'dev'
                }
            }
            steps {
                script {
                    echo "deploying the application..."
                    
                }
            }
        }

    }
}

