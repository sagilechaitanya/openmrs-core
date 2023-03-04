pipeline {
  agent {label'chaitanya'} 
  tools {jdk 'jdk-8'}
  stages {
    stage('vcs') {
        steps {
          git url: 'https://github.com/sagilechaitanya/openmrs-core.git',
            branch: 'declarative'  
        }
    } 
    stage('mvnpackage') {
      steps {
        sh 'mvn clean package'
      }  
    }
  } 
}