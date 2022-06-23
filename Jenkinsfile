pipeline {
  agent any
  stages {
	stage("build"){
	   steps {
	      sh "python3 -m pip install -r requirements.txt --user"
	      sh "python3 -m py_compile apicall.py"
	}
      }
	stage("Test"){
	  steps {
	      sh "python3 -m pytest"
        }
      }
	stage("Post-testing"){
	  steps {
            echo "Build # $BUILD_NUMBER is successful"
       }
     }
    }
  }
}