pipeline{
    agent any
        stages 
        {
             stage('ContinuousDownload')
           {
               steps
                {
               git 'https://github.com/8080ksr/maven.git' 
                }
           }
           stage('ContinuousBuild')
           {
              steps
             {
               sh 'mvn package'
            }
        }  
    }
}
