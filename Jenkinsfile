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
        tool: ('jdk-8')
      }  
    }
    stage('mvnpackage') {
      steps {
        sh 'mvn clean package'
      }  
    }
  } 
}