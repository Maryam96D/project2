pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Installing dependencies...'
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
                // اگر تستی دارید، می‌توانید دستور اجرای تست‌ها را اینجا اضافه کنید.
            }
        }
        stage('Deploy') {
            when {
                branch 'master'
            }
            steps {
                echo 'Deploying application on master branch...'
                // دستورات مورد نیاز برای استقرار (برای مثال ساخت Docker image یا استقرار در سرور)
            }
        }
    }
    
    post {
        always {
            echo 'Pipeline finished.'
        }
    }
}
