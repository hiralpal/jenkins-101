pipeline {
    agent any
    
    triggers {
        pollSCM '* * * * *'
    }
    stages {
        stage('Build') {
            steps {
                echo "Building.."
                bat '''
                cd myapp
                pip install -r requirements.txt
                '''
                
            }
        }
        stage('Test') {
            steps {
                echo "Testing.."
                bat'''
                cd myapp
                python hello.py
                python hello.py --name=Hiral
                '''
            }
        }
        stage('Deliver') {
            steps {
                echo 'Deliver....'
                bat'''
                echo "doing delivery stuff.."
                '''
            }
        }
    }
}
