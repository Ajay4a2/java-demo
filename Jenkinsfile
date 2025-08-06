pipeline {
    agent any

    stages {
        stage('Install JDK 9') {
            steps {
                echo '📥 Downloading and Extracting JDK 9.0.4'
                sh '''
                    curl -L -b "oraclelicense=accept-securebackup-cookie" \
                    -o jdk-9.0.4_linux-x64_bin.tar.gz \
                    https://download.oracle.com/otn/java/jdk/9.0.4+11/b4a5c12014d54f4e9a5f42b269d5c7ed/jdk-9.0.4_linux-x64_bin.tar.gz

                    tar -xzf jdk-9.0.4_linux-x64_bin.tar.gz
                '''
            }
        }

        stage('Compile') {
            steps {
                echo '📦 Compiling Sample.java'
                sh './jdk-9.0.4/bin/javac Sample.java'
            }
        }

        stage('Run') {
            steps {
                echo '🚀 Running Java Application'
                sh './jdk-9.0.4/bin/java Sample'
            }
        }
    }
}
