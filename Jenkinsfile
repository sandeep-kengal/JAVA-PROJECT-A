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
       sh '''mvn clean install'''          
      }
    }
    stage ( 'deploy' ) {
      steps {
        sshagent(['slave-tomcat']) {
      sh '''scp -o StrictHostKeyChecking=no /var/lib/jenkins/workspace/Build-Deploy-Test/helloworld/1project/dist/*.war ec2-user@172.31.37.18:/opt/tomcat9/webapps''' 
    
  }
}

