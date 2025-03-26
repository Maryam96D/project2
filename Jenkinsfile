pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // استفاده از Credential برای دسترسی SSH به مخزن
                git credentialsId: 'a7b55f56-fe09-4503-837e-a11eea1d2fe3', url: 'git@github.com:Maryam96D/project2.git'
            }
        }
        stage('Build') {
            steps {
                echo 'Installing dependencies...'
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
                // در صورت نیاز دستور اجرای تست‌ها را اضافه کنید.
            }
        }
        stage('Deploy') {
            when {
                branch 'main'
            }
            steps {
                echo 'Deploying application on main  branch...'
                // دستورات مورد نیاز برای استقرار را اینجا اضافه کنید.
            }
        }
    }
    
    post {
        always {
            echo 'Pipeline finished.'
        }
    }
}

