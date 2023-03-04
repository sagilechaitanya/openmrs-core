pipeline {
  agent {label'chaitanya'} 
  stages {
    stage('vcs') {
        steps {
          git url: 'https://github.com/sagilechaitanya/openmrs-core.git',
            branch: 'declarative'  
        }
    }
    stage('exportpath') {
      steps {
        sh 'export PATH="/usr/lib/jvm/java-8-openjdk-amd64/jre/bin/:$PATH"'
      }  
    }
    stage('mvnpackage') {
      steps {
        sh 'mvn clean package'
      }  
    }
  } 
}