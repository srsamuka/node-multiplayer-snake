node ('app-server'){  
    def app
    stage('Cloning Git') {
        checkout scm
    }  
    
    stage('Build-and-Tag') {
        app = docker.build("amirt96/snake")
    }
    stage('Post-to-dockerhub') {
        
     docker.withRegistry('https://registry.hub.docker.com', '2105c6a9-11f8-4c79-9049-bc1d3f88b649') {
            app.push("latest")
        			}
         }
    
    stage('Pull-image-server') {
        
         sh "docker-compose down"
         sh "docker-compose up -d"	
      }
     
}
