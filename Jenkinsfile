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
               stage('ContinuousDeployment')
        {
            steps
            {
                deploy adapters: [tomcat9(credentialsId: '11edb6fd-2916-446d-9b05-f2f79ff57930', path: '', url: 'http://3.143.147.60:8080/')], contextPath: 'test', war: '**/*.war'
               }
        }
        }  
    }
}
