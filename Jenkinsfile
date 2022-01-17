node {
    def app

    stage('Clone repository') {

        checkout scm
    }

    stage('Build image') {

        app = docker.build("exskandr/test_for_devops")
    }

   // stage('Push image') {

     //   docker.withRegistry('https://registry.hub.docker.com', 'docker-hub') {
       //     app.push("redis31122021")
         //   } 
           //     echo "Trying to Push Docker Build to DockerHub"
    //}

    stage('Deploy') {

        sh 'docker-compose -f docker-compose.yml up -d'
    }

}
