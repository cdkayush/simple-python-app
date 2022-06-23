pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
	            sh "python3 -m pip install -r requirements.txt --user"
	            sh "python3 -m py_compile apicall.py"
            }
        }
        stage('Test') {
            steps {
	            sh "python3 -m pytest"
            }
        }
        stage('Print success msg') {
            steps {
                echo "Build# $BUILD_NUMBER is successful"
            }
        }
    }
}
