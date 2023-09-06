pipeline {
agent any
environment{DOCKERHUB_CREDENTIALS=credentials('dockerhub')}
 stages {
        stage('Build') {
			steps{   
			
			sh ' docker build -t chetouiiftikhar/img:img . '
                      } }
	  stage('login') {
			steps{   
			
			sh ' echo $DOCKERHUB_CREDENTIALS_PSW | docker login -u $DOCKERHUB_CREDENTIALS_USR --password-stdin '
                      } }
         stage('push') {
			steps{
			sh ' docker push chetouiiftikhar/img:img . '

                      }}
          stage('run') {
			steps{
			sh ' docker run -dit chetouiiftikhar/img:img '

                      }}
                      
}
}

