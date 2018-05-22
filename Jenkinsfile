pipeline {
    agent {
        docker {
            image 'maven:3-alpine' 
            args '-v /root/.m2:/home/jenkins/.m2'
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package' 
            }
        }
	stage('Azaza') {
	    steps {
	        sh 'chmod a+rwx /home/jenkins/.m2 && echo 5 >> /home/jenkins/.m2/aaa'
	    }
	}
    }
}
