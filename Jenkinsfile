pipeline{
    agent any
    tools{
        jdk 'jdk17'
        nodejs 'node16'
    }
    environment {
        SCANNER_HOME=tool 'sonar-scanner'
    }
    stages {
        stage('clean workspace'){
            steps{
                cleanWs()
            }
        }
        stage('Checkout from Git'){
            steps{
                git branch: 'main', url: 'https://github.com/mudit097/Reddit-Clone-apps.git', credentialsId: '<your-credentials-id>'
            }
        }
        stage("Sonarqube Analysis "){
            steps{
                withSonarQubeEnv('sonar-server') {
                    sh """$SCANNER_HOME/bin/sonar-scanner -Dsonar.projectName=Reddit -Dsonar.projectKey=Reddit"""
                }
            }
        }
        stage("quality gate"){
           steps {
                script {
                    waitForQualityGate abortPipeline: false, credentialsId: 'Sonar-token' 
                }
            } 
        }
        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }
        stage('OWASP FS SCAN') {
            steps {
                dependencyCheck additionalArguments: '--scan ./ --disableYarnAudit --disableNodeAudit', odcInstallation: 'DP-Check'
                dependencyCheckPublisher pattern: '**/dependency-check-report.xml'
            }
        }
        stage('TRIVY FS SCAN') {
            steps { 
                sh """trivy fs . > trivyfs.txt"""                           
            }
        }
        stage("Docker Build & Push"){
            steps{
                script{
                   withDockerRegistry([credentialsId: 'dockerhub-credentials', url: 'https://index.docker.io/v1/']){ 
                       sh "docker build -t reddit ."
                       sh "docker tag reddit timour259/reddit:latest "
                       sh "docker push timour259/reddit:latest "
                    }
                }
            }
        }
        stage("TRIVY"){
            steps{
                sh "trivy image timour259/reddit:latest > trivy.txt" 
            }
        }
    }
}