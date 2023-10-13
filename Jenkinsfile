pipeline{
    agent any

    tools{
        maven "maven"
    }
    environment{
        VERSION_NAME="1.2"
    }
    stages{
        stage("compile"){
            steps{
                sh "javac Test.java"
                SH 'echo "${VERSION_NAME}"'
            }
        }

        stage("run"){
            steps{
                sh "java Test"
            }
        }
    }

    post{

        always{
            sh 'echo "always"'     
        }
        success{
            sh 'echo "success"'     
        }

        failure{
            sh 'echo "failure"'
        }
    }
}