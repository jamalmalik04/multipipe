node('master') 
{
    stage('Continuous Download') 
	{
    git 'https://github.com/sunildevops77/maven.git'
	}
    stage('Continuous Build') 
	{
    sh label: '', script: 'mvn package'
	}
    stage('contunus deployment')
        {
    sh 'scp /home/ubuntu/.jenkins/workspace/pipelinejob1/webapp/target/webapp.war ubuntu@172.31.19.244:/var/lib/tomcat8/webapps/qamulti.war' 
        }
}



