pipeline {
    agent any
    stages {
        stage ("Build") {
            steps {
                sh 'docker build -t saikumarbodla/abinay:bus .'
            }
        }
        
        stage ("Deploy") {
            steps {
                sh 'docker run -itd --name bus -p 8888:80 saikumarbodla/abinay:bus'
            }
        }
    }
}
