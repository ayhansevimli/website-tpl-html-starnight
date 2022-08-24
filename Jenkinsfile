pipeline {
    agent any
    
//    environment {
//        WORKSPACE = '/var/www/html'
//        DB_ENGINE        = 'sqlite'
//    }
    
    stages {
        stage('Hello') {
            steps {
                echo 'Hello Everyone..'
                sh 'printenv'
//                sh 'pwd'
//                sh 'cd /var/www/html'
//                sh 'pwd'
//                sh 'ls /var/www/html'
            }
        }
        stage('Build') {
            steps {
                ws("/var/www/html") 
                {
                    echo 'Building..'
//                  git https://github.com/ayhansevimli/website-tpl-html-starnight.git
                    git url: 'https://github.com/ayhansevimli/website-tpl-html-starnight.git', branch: 'main'
                }
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
        stage('Goodbye') {
            steps {
                echo 'Bye....'
            }
        }
    }
}
