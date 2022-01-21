pipeline {
 agent any
  environment {
     NEW_VERSION = "1.1"
  }
 tools {
  maven "maven"
 }
 stages {
  stage ('build') {
   steps {
   echo "This is build stage"
   sh 'printenv'
   sh "mvn --version"
     }
   }
  stage ('test') {
    when {
      expression {
         STAGE_NAME == "QA" || STAGE_NAME == "UAT"
      }

    }
   steps {
   echo "This is test stage"
     }
   }
  stage ('deploy') {
   steps {
    echo "This is deploy stage"
    echo "Deployed version is ${NEW_VERSION}"
    }
  }
 }
}
