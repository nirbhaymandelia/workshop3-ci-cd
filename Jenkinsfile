pipeline{
    agent any
    
    stages{
        stage('Installing NPM dependencies'){
            agent {
          docker {
                image 'node:12-slim'
            }
        } 
            steps {
                sh 'npm install'
            }
        }
         stage('Run Unit Test'){
        agent {
            docker {
                image 'node:12-slim'
            }
        } 
            steps {
                sh 'npm run test'
            }
        }
        stage('Run Coverage Test'){
            agent {
            docker {
                image 'node:12-slim'
            }
        }
            steps {
                sh 'npm run test:coverage'
            }
        }
        stage('Run Sonar Analysis'){
            steps {
                sh 'npm run sonar'
            }
        }
    }
}