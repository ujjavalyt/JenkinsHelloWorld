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
  }
}
