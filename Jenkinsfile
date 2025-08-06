pipeline {
    agent any

    stages {
        stage('Install OpenJDK') {
            steps {
                echo '📥 Downloading and Extracting OpenJDK 11'
                sh '''
                    curl -L -o openjdk11.tar.gz https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.20.1+1/OpenJDK11U-jdk_x64_linux_hotspot_11.0.20.1_1.tar.gz
                    tar -xzf openjdk11.tar.gz
                    mv jdk-11* openjdk11
                '''
            }
        }

        stage('Compile') {
            steps {
                echo '📦 Compiling Sample.java'
                sh './openjdk11/bin/javac Sample.java'
            }
        }

        stage('Run') {
            steps {
                echo '🚀 Running Java Application'
                sh './openjdk11/bin/java Sample'
            }
        }
    }
}
