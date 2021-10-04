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
        bat "java HelloWorld"
        echo "Project executed"
    }
  }
}
