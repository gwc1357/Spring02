pipeline {
    agent any
    
    tools {
        maven 'my-maven'  // 젠킨스에서 설치한 이름
    }
    environment {
        APP_NAME = 'ex02-app'
        DOCKER_TAG = 'latest'
        IMAGE_NAME = "gwc11/${APP_NAME}:${DOCKER_TAG}"
        TARGET_HOST = '192.168.56.107'
        TARGET_USER = 'vagrant'
        PORT = '8081'
    }
    stages {
        stage('0. 자동화 확인1') { steps { echo '스테이지 출발' } }
        
        stage('1. Build') {
            steps {
                echo 'Maven으로 빌드 시작'
                sh 'mvn clean package'
            }
        }      
    }
}


















