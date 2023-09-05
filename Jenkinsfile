pipeline {
agent any
 stages {
        stage('Build') {
			steps{   
			
			sh ' docker build -t chetouiiftikhar/img:img . '
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

