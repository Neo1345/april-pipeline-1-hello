pipeline
{
agent any
stages
{
    stage ('sch-checkout')
    {  steps
         { sh 'echo code reading' }
        
    }   
    stage ('compile the code')
    { steps 
           { sh 'echo code compilation' }

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
