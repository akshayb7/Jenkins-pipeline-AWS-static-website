pipeline {
    agent any
    stages {
        stage('Upload to AWS') {
            steps{
                retry(5){
                    withAWS(region:'us-east-2', credentials:'aws-static'){
                        s3Upload(file: 'index.html', bucket: 'jenkins-static-website-aws', path:'')
                    }
                }
            }
        }
    }
}