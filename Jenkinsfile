pipeline {
    agent any
    stages {
        stage('relative path') {
            steps {
                sh 'echo "changing permissions of script find"'
                sh "chmod +x find.sh"
                echo "my workspace"
                echo "${WORKSPACE}"
                echo "FIND NUMBER OF USERS ON THE SYSTEM WITH RELATIVE PATH"
                sh "./find.sh > users_Rel.out"
             }
        }
        stage('absolute path') {
            steps {
                echo "FIND NUMBER OF USERS ON THE SYSTEM WITH ABSOLURE PATH"
                sh "${WORKSPACE}/find.sh > users_abs.out"
            }
        }
        stage('GO TO path') {
            dir("${WORKSPACE}")
            steps {
                echo "CHANGed DIR"
                sh "./find.sh > users_ch_dir.out"
            }
        }
                   
    }
    
    post {
        always {
         archiveArtifacts artifacts : '*.out'
        }
    }
}
