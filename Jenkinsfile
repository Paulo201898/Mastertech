pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'git clone https://github.com/Paulo201898/Mastertech.git /tmp/teste/'
                sh 'docker build -t mastertech /tmp/teste/'
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
                sh 'docker run -d -p 8085:80 mastertech'
            }
        }
    }
}
