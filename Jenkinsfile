pipeline
{
agent any
stages
{
    stage ('sch-checkout')
    {  steps
         { sh 'echo code reading' }
         {  git branch: 'master', url: 'https://github.com/Neo1345/april-pipeline-1-hello' }
        
    }   
    stage ('compile the code')
    { steps 
           { sh 'echo code compilation' }
     {withMaven(globalMavenSettingsConfig: '', jdk: 'jdk-1.8', maven: 'my_maven', mavenSettingsConfig: '', traceability: true) {
    sh 'mvn test'
}}

    }   
    stage('executing functional & component testing ')  
    {
     parallel
           {
             stage ('executing functional'){
                 steps { sh 'echo executing functional' }} 

             stage ('component testing') {
                 steps { sh 'echo component testing' }}
           }
    }
}
}
