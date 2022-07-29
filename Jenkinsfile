pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                sh 'echo "hello"'
                echo "my workspace"
                echo "${WORKSPACE}"
                echo "FIND NUMBER OF USERS ON THE SYSTEM"
                sh "./find.sh"
            }
        }
    }
}
