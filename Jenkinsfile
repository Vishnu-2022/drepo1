pipeline {
    agent {
  label 'node1'
}
	
	tools {
  git 'Default'
}

    stages {
        stage('Pull From Git') {
            steps {
                git branch: 'main', credentialsId: 'a380b5b2-7c98-451c-810b-a7358629f797', url: 'https://github.com/Vishnu-2022/drepo1'
            }
        }
        stage('Docker build') {
            steps {
                
                sh 'sudo chmod 666 /var/run/docker.sock'
                
				sh '''sudo docker build -t vishnu2022/jenkinsscriptrepo1:latest .
'''
            }
        }
    }
}
