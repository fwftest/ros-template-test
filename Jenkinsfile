// Jenkinsfile

pipeline {
    agent any // 指定在任何可用的 agent 上执行

    stages {
        stage('Checkout') {
            steps {
                // 从 GitHub 仓库拉取最新的代码
                checkout scm
                echo 'Checked out the latest code.'
            }
        }
        stage('Build') {
            steps {
                // 这是一个示例构建步骤，可以替换为你的实际命令
                echo 'Building the application...'
                // 比如对于 Maven 项目: sh 'mvn clean install'
                // 比如对于 Node.js 项目: sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                // 这是一个示例测试步骤
                echo 'Running tests...'
                // 比如对于 Maven 项目: sh 'mvn test'
                // 比如对于 Node.js 项目: sh 'npm test'
            }
        }
        stage('Deploy') {
            steps {
                // 这是一个示例部署步骤
                echo 'Deploying the application...'
            }
        }
    }

    post {
        // 无论构建结果如何，总会执行
        always {
            echo 'Pipeline finished.'
        }
        // 构建成功时执行
        success {
            echo 'Pipeline succeeded!'
        }
        // 构建失败时执行
        failure {
            echo 'Pipeline failed!'
        }
    }
}
