pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'sudo docker build -t mastertech .'
                }


        }
        stage('Delivery'){
        input {
                message "Quer fazer deploy em producao?"
                ok "sim"
            }
	steps {
		sh 'echo enviando para producao'

		}
		}


        stage('Deploy') {
            steps {
                sh 'sudo docker run -d -p 8085:80 mastertech'
            }
        }
    }
}
