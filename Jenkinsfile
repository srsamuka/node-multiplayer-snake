node ('Ubuntu-app-agent'){  
    //def app
    stage('Cloning Git') {
        /* Let's make sure we have the repository cloned to our workspace */
       checkout scm
    }  
    stage('Build-and-tag'){
        sh 'echo Build-and-tag'
        //build 'SECURITY-SAST-SNYK'
    }

    
    stage('Build-and-Tag2') {
        sh 'echo Build-and tag2'
    /* This builds the actual image; synonymous to
         * docker build on the command line 
        app = docker.build("amrit96/snake")*/
    }
    stage('Post-to-dockerhub') {
        sh 'echo Post-to-dockerhub'
     /*docker.withRegistry('https://registry.hub.docker.com', 'training_creds') {
            app.push("latest")*/
        			}
         }
    stage('SECURITY-IMAGE-SCANNER'){
        sh 'echo SECURITY-IMAGE-SCANNER'
        //build 'SECURITY-IMAGE-SCANNER-AQUAMICROSCANNER'
    }
  
    
    stage('Pull-image-server') {
        sh 'Pull-image-server'
       /*  sh "docker-compose down"
         sh "docker-compose up -d"	*/
      }
    
    stage('DAST')
        {
        build 'SECURITY-DAST-OWASP_ZAP'
        }
 
}
