pipeline{
    agent any
    stages{
        stage('Checkout'){
            steps{
                git credentialsId: 'github', url: 'https://github.com/jenkins-pipeline86/micro-2.git'
            }
            
        }
        stage('Cat Jenkins file'){
            when {
                branch pattern: 'master', comparator: 'REGEXP'
            }
            steps{
                sh 'echo "Hello from micro-1"'
                sh 'cat Jenkinsfile'
            }
        }
        
        stage('Cat Jenkins file'){
            when {
                branch pattern: 'fix.*', comparator: 'REGEXP'
            }
            steps{
                sh 'echo "Hello from micro-1"'
                sh 'cat Jenkinsfile'
            }
        }
    }

}