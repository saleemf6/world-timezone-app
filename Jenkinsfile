pipeline
{
	agent any
	tools{
		maven '3.8.2'
		jdk 'jdk8'
		}
	stages{
		stage('Build Application'){
		steps{
		bat 'mvn clean install'
		}
		}
		
		stage('Deploy Application To Mulesoft Cloudhub'){
		steps{
		bat 'mvn package deploy -DmuleDeploy'
		}}
		
		stage('Perform Regression Testing'){
		steps{
		bat 'newman run "C:\\Users\\Fahim Saleem\\Documents\\POSTMAN COLLECTION\\worldtimezone.postman_collection.json" --disable-unicode'
		
		}}
	
	}


}