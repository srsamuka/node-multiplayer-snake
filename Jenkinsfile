node ('app-server'){  
    def app
    stage('Cloning Git') {

       checkout scm
    }  
    
    stage('Build-and-Tag') {
        app = docker.build("srsamuka/myrepo")
    }
    stage('Post-to-dockerhub') {
        
     docker.withRegistry('https://registry.hub.docker.com', 'docker_hub_credentials') {
            app.push("latest")
        			}
         }
    
    stage('Pull-image-server') {
        
         sh "docker-compose down"
         sh "docker-compose up -d"	
      }
     
}
