pipeline {
 agent any
 stages {
  stage ('build') {
   steps {
   echo "This is build stage"
   sh 'printenv'
     }
   }
  stage ('test') {
    when {
      expression {
         STAGE_NAME == "test" || STAGE_NAME == "test"
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
