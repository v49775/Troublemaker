pipeline{
    agent any
    stages {
    
        stage('Setup Python Virtual ENV for dependencies'){
      stage('Check Files') {
            steps {
                sh 'ls -al'
            }
        }
       
      steps  {
            sh '''
            ls
            chmod +x envsetup.sh
            ./envsetup.sh
            '''}
        }
        stage('Setup Gunicorn Setup'){
            steps {
                sh '''
                chmod +x gunicorn.sh
                ./gunicorn.sh
                '''
            }
        }
        stage('setup NGINX'){
            steps {
                sh '''
                chmod +x nginx.sh
                ./nginx.sh
                '''
            }
        }
    }
}
