pipeline {
    agent any

    tools {
        // Maven을 사용하는 경우, Jenkins에서 설정된 Maven 버전의 이름을 지정합니다.
        maven "M3"
    }

    stages {
        stage('Clone repository') {
            steps {
                git 'https://github.com/g-hyeong/hello-world-greeting.git'
            }
        }

        stage('Build') {
            steps {
                // Maven 프로젝트를 빌드하는 명령
                sh 'mvn clean package'
            }
        }

        stage('Test') {
            steps {
                // Maven 프로젝트의 테스트를 실행하는 명령
                sh 'mvn test'
            }
        }
    }
}
