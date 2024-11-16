pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                git url: 'https://github.com/vishnu148/week-4', branch: 'main'
            }
        }
        stage('Execute Java Program') {
            steps {
                script {
                    def javaFile = 'YourJavaProgram.java'
                    bat "javac ${javaFile} && java ${javaFile.replace('.java', '')}"
                }
            }
        }
        stage('Execute Python Program') {
            steps {
                script {
                    def pythonFile = 'YourPythonScript.py'
                    bat "python ${pythonFile}"
                }
            }
        }
    }
}
