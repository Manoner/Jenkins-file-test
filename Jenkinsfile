pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'echo "Hello World"'
                sh '''
                    echo "Multiline shell steps works too"
                    ls -lah
                '''
            }
        }
        stage('Deploy'){
            steps{
                retry(3){
                    sh 'echo retry 3 times.'
                }
                timeout(time:3,unit:'MINUTES'){
                    sh 'echo timeout 3 minutes.'
                }
            }
        }
    }
}
