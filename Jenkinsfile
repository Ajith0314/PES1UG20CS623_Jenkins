pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ -c pes1ug20cs623.cpp - error'
                sh 'g++ -o pes1ug20cs623 pes1ug20cs623.cpp'
                echo 'Build successful'
            }
        }
        stage('Test') {
            steps {
                sh './pes1ug20cs623'
                echo 'Test was successful'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploy steps successful'
            }
        }
        
    }
    post{
       failure{
      echo 'Pipelined failed'
       }
    }
}
