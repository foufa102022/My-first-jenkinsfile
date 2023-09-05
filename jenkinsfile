pipeline {
agent any

 stages {
        stage('Build') {
        
			
			sh ' docker build -t chetouiiftikhar/img:img . '
                      }
         stage('push') {
			
			sh ' docker push -t chetouiiftikhar/img:img . '

                      }
          stage('run') {
			
			sh ' docker run -dit chetouiiftikhar/img:img '

                      }
                      
}
}
