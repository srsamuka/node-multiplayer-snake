node ('master'){  
    //def app
    stage('Cloning Git') {
        /* Let's make sure we have the repository cloned to our workspace */
       checkout scm
    }  
    stage('Build-and-tag'){
        sh 'echo Build-andT-tag'
        /*build 'SECURITY-SAST-SNYK'*/
    }

    
    stage('Build-and-Tag2') {
    /* This builds the actual image; synonymous to
         * docker build on the command line */
        //app = docker.build("amrit96/snake")
    }
    stage('Post-to-dockerhub') {
    sh 'echo Post-to-dockerhub'
    /* docker.withRegistry('https://registry.hub.docker.com', 'training_creds') {
            app.push("latest")*/
        			}
         }
    stage('SECURITY-IMAGE-SCANNER'){
       sh 'echo One-More Phase'
        // build 'SECURITY-IMAGE-SCANNER-AQUAMICROSCANNER'
    }
  
    
    stage('Pull-image-server') {
        sh 'echo Pull-image')
         /*sh "docker-compose down"
         sh "docker-compose up -d"	*/
      }
    
    stage('LAST') {
        sh 'echo That-is-it'
        //build 'SECURITY-DAST-OWASP_ZAP'
        
    }
 
}
