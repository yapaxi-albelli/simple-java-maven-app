pipeline {
    agent {
        docker {
            image 'maven:3-alpine' 
            args '-v /root/.m2:/var/lib/jenkins/workspace'
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
	        sh 'echo 5 >> ./aa.txt'
	    }
	}
    }
}
