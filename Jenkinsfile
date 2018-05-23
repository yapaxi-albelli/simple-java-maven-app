pipeline {
    agent {
        docker {
            image 'maven:3-alpine' 
            args '-v /root/.m2:/var/lib/jenkins/workspace/simple-java-maven-app-xxx'
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
	        sh 'mkdir /var/lib/jenkins/workspace/simple-java-maven-app-xxx && echo 100500 >> /var/lib/jenkins/workspace/simple-java-maven-app-xxx/aa.txt'
	    }
	}
    }
}
