pipeline {
  agent any
 
 
    tools {
      gradle 'gradle'
      jdk 'JDK'
      }
      
      stages {
         stage('Checkout'){
         steps{
          git branch: 'main', url:'https://github.com/DakshhBN/Lab2.git'
          }}
          
          stage('Build'){
          steps{
          sh 'gradle build'
          }}
          
          stage('Test'){
          steps{
          sh 'gradle run'
          }}
          
          stage('Run Application')
         {
         steps{
         sh 'gradle display'
         }}
}
 post {
 success{
 echo 'Build and deployment successful!'
 }
 failure{
 echo 'Build failed!'
 }}}










