pipeline{
    agent any 
    stages{
        stage('Installing NPM dependencies'){
            steps {
                sh 'export PATH=/usr/local/bin  npm install'
                sh 'npm install'
            }
        }
         stage('Run Unit Test'){
            steps {
                sh 'export PATH=/usr/local/bin  npm install'
                sh 'npm run test'
            }
        }
        stage('Run Coverage Test'){
            steps {
                sh 'export PATH=/usr/local/bin  npm install'
                sh 'npm run test:coverage'
            }
        }
        stage('Run Sonar Analysis'){
            steps {
                sh 'export PATH=/usr/local/bin  npm install'
                sh 'npm run sonar'
            }
        }
    }
}