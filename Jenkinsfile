pipeline{

    agent any

    stages {

        stage("build") {

            steps {
            sh 'npm i'
            sh 'npm run build'
           

            }

        }


        stage("deploy") {

            steps {
            
	sh " ansible-playbook angular-app-deploy.yml --key-file /var/lib/jenkins/id_rsa "

            }

        }

    }

}
