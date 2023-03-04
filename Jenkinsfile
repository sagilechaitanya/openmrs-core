node('chaitanya') {
  stage('vcs')  {
   git url: 'https://github.com/sagilechaitanya/openmrs-core.git',
       branch: 'sricpted'
  } 
  stage('exportpath') {
    tool: ('jdk-8')
  }
  stage('mvnpackage') {
    sh 'mvn clean package'
  }
}
