pipeline{
    agent any
    environment {
      name = "shellway"
      password = "123456"
    }
    stages{
        stage('环境'){
            steps{
                echo "环境监测"
                sh 'printenv'
                echo "${name}"
                echo "$password"

            }
        }
        stage('编译'){
            agent {
                docker { image 'maven:3-alpine'}
            }
            steps{
                echo "编译"
                sh "pwd&&ls"
                sh "pwd&&ls -alp"
                sh "mvn -v"
            }
        }
        stage('测试'){
            steps{
                echo "测试"
            }
        }
        stage('打包'){
            steps{
                echo "打包"
            }
        }
        stage('部署'){
            steps{
                echo "部署"
            }
        }
    }
}