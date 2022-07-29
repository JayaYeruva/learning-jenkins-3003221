pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                sh 'echo "changing permissions of script find"'
                sh "chmod +x find.sh"
                echo "my workspace"
                echo "${WORKSPACE}"
                echo "FIND NUMBER OF USERS ON THE SYSTEM"
                sh "./find.sh"
            }
        }
    }
}
