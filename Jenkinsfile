pipeline{
agent any
tools{
maven 'Maven'
}
stages{
stage('Checkout')
{
steps{
git branch:'master',url:'https://github.com/Samiksha201104/MyGradlePApp.git'
}}
stage('Build')
{
steps{
sh 'mvn clean package'
}
}
stage('Test')
{
steps{
sh 'mvn test'
}
}
stage('Run')
{
steps{
sh 'cp target/MyMavenWebApp01.war /opt/tomcat/webapps/'
}
}}
post
{
success{
echo 'Build success'
}
failure{
echo 'build failure'
}}}
