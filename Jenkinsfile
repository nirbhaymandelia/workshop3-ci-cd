pipeline{
    agent any

    stages{
        stage('Installing NPM dependencies'){

            steps {
                sh 'npm install'
            }
        }
         stage('Run Unit Test'){

            steps {
                sh 'npm run test'
            }
        }
        stage('Run Coverage Test'){

            steps {
                sh 'npm run test:coverage'
            }
        }
        stage('Run Sonar Analysis'){
            steps {
                echo 'npm run sonar'
            }
        }
    }
}
