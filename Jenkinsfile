pipeline{
    agent any
    stages {
        stage('Check Files') {
            steps {
                sh 'ls -al'
            }
        }
        stage('Setup Python Virtual ENV for dependencies'){
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
