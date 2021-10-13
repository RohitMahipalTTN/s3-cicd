pipeline {
    agent any

    stages{
        stage('deploy to S3'){
            steps{
                sh 'aws s3 cp public/index.html s3://static-website-automation'
                sh 'aws s3 cp public/error.html s3://static-website-automation'
            }
        }
    }
    post{
        always{
            cleanWs disableDeferredWipeout: true, deleteDirs: true
        }
    }

}
