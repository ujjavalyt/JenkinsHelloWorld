pipeline {
 agent any
  stages {
    stage("Compile Project") {
      steps {
       bat "javac HelloWorld.java"
        echo "Project Compiled"
      }
    }
    stage("Run Project") {
      steps {
       input ("Do you want to execute the project?")
        bat "java HelloWorld"
        echo "Project executed"
      }
    }
   stage("Email Execution Status") {
    steps {
     mail bcc: '', body: 'Execution aborted by user for job ${env.JOB_NAME} - Build# ${env.BUILD_NUMBER} \n\n Check console output at ${env.BUILD_URL} to view the results.', cc: '', from: '', replyTo: '', subject: 'Execution aborted', to: 'ujjavalyt@gmail.com'
    }
   }
  }
}
