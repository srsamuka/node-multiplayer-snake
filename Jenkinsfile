node ('application'){  
    def app
    stage('Cloning Git') {
        //sh 'echo c'
    checkout scm
    }  
    
    stage('Build-and-Tag') {
        //sh 'echo Build-tag'
        app = docker.build("srsamuka/snake")        
    }
    stage('Post-to-dockerhub') {
        //sh 'echo Post-to-docker'
        docker.withRegistry('https://registry.hub.docker.com', 'dockerhub_credentials') {
            app.push("latest")
            }
    }
    
    stage('Pull-image-server') {
        //sh 'echo Pull-image'
         sh "docker-compose down"
         sh "docker-compose up -d"
    }
     
}
