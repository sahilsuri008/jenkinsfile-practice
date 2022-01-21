pipeline {
 agent any
 stages {
  stage ('build') {
   steps {
   echo "This is build stage"
     }
   }
  stage ('test') {
    when {
      expression {
         BRANCH_NAME == "main" || BRANCH_NAME == "master"
      }

    }
   steps {
   echo "This is test stage"
     }
   }
  stage ('deploy') {
   steps {
    echo "This is deploy stage"
    }
  }
 }
}
