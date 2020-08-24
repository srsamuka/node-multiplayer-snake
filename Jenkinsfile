node ('app-server'){  
    //def app
    stage('Cloning Git') {
        //sh 'echo c
    checkout scm
    }  
    
    stage('Build-and-Tag') {
        sh 'echo Build-tag'
        //app = docker.build("srsamuka/myrepo")
    }
    stage('Post-to-dockerhub') {
        sh 'echo Post-to-docker'
     /*docker.withRegistry('https://registry.hub.docker.com', '2105c6a9-11f8-4c79-9049-bc1d3f88b649') {
            app.push("latest")
        			}*/
         }
    
    stage('Pull-image-server') {
        sh 'echo Pull-image'
         /*sh "docker-compose down"
         sh "docker-compose up -d"	*/
      }
     
}
