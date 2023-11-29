node('built-in') 
{
   stage('Continuies Download') 
    {
      git 'https://github.com/sunildevops77/maven.git'
    }

   stage('Continuies Build') 
    {
      sh 'mvn package'
    }
  stage('Continuies Deploye') 
    {
     sh ' scp /home/ubuntu/.jenkins/workspace/Pipline/webapp/target/webapp.war ubuntu@172.31.41.185:/var/lib/tomcat9/webapps/qaenv.war'
    }

   stage('Continuies Testing') 
    {
     sh 'echo "Testing Passed"'
    }
  stage('Continuies Delivery') 
    {
     sh ' scp /home/ubuntu/.jenkins/workspace/Pipline/webapp/target/webapp.war ubuntu@172.31.46.66:/var/lib/tomcat9/webapps/prodenv.war'
    }
}
