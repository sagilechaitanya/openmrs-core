pool: "Default"
trigger: 
  - azure
stages:  
  - stage:"vcs"
    jobs:
       - job: "vcs clone"
         steps:
           - task: Maven@3
             inputs: 
               mavenPOMFile: 'pom.xml'
               goals: 'package'
               publishJUnitResults: true
               testResultsFiles: '**/surefire-reports/TEST-*.xml'
               javaHomeOption: 'Path'
               jdkVersionOption: '1.8'
               jdkDirectory: "/usr/lib/jvm/java-8-openjdk-amd64"
               mavenVersionOption: 'Path'
               MavenDirectory: '/usr/share/maven'
           - task: PublishPipelineArtifact@1  
            inputs:
               targetPath: '$(Pipeline.Workspace)'
               artifact: "chaitu"
               publishLocation: 'pipeline' 
