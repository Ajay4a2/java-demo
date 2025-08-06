pipeline {
    agent any

    tools {
        jdk 'jdk-21' // Use the JDK you configured in Jenkins Global Tool Configuration
    }

    stages {
        stage('Compile') {
            steps {
                echo '📦 Compiling Sample.java'
                sh 'javac Sample.java'
            }
        }

        stage('Run') {
            steps {
                echo '🚀 Running Java Application'
                sh 'java Sample'
            }
        }
    }
}
