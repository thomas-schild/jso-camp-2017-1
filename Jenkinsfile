pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying'
            }
        }
    }
    post {
        always {
            echo 'POST-step which runs always'
        }
        success {
            echo 'POST-step which runs on successful build'
        }
        failure {
            echo 'POST-step which runs when building the pipeline failed'
        }
        unstable {
            echo 'POST-step which runs when build is marked as unstable'
        }
        changed {
            sh '''
            echo "POST-step which runs when if the state of the Pipeline has changed"
            echo "e.g., if the Pipeline was previously failing but is now successful"
            '''            
        }
    }    
}
