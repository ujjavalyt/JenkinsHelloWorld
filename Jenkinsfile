pipeline {
 agent any
  stages {
   stage("Parallel Execution") {
    steps {
     parallel(
      a: {
       bat "javac HelloWorld.java"
        echo "Project Compiled"
      }
      b: {
        bat "java HelloWorld"
        echo "Project executed"
      }
      )
    }
   }
  }
}
