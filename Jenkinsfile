pipeline {
  agent any
  stages {
    stage ('git') {
      steps {
        git branch: 'main', url:'https://github.com/sandeep-kengal/JAVA-PROJECT-A.git'
      }
    }
    stage ('build') {
      steps {
       sh '''mvn clean test'''          
      }
    }
    
    
  }
}

