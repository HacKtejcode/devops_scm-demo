pipeline{
    agent any


    stages{
        stage('Use jenkins Java 17'){
            tools{
                jdk 'JAVA-17'
            }
            steps{
                bat 'java -version'
                bat 'javac -version'
                bat 'echo JAVA_HOME=%JAVA_HOME%'
                bat "echo Using Java 17 from Jenkins"
                }
	   }

        stage('Use Java 26'){
             steps{
                bat 'echo using system java version'
                bat '"C:\\Program Files\\Java\\jdk-26.0.2\\bin\\java.exe" -version'
                bat "echo Using Java 26 from the system"
                }
	    }

        stage('Use jenkins Java 17 again'){
             tools{
                jdk 'JAVA-17'
            }
            steps{
                bat 'echo Again using Java 17'
                bat 'java -version'
            }
        }

    }

    post{
        success{
            echo 'Pipeline completed successfully!'
        }
        failure{
            echo 'Pipeline failed'
            }
        }
}
