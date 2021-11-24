node{
    stage('SCM Checkout'){
        sh 'echo "started"'
        git credentialsId: 'Git_token', url: 'https://github.com/AnilComakeit/Docker-website.git'


        
    }
    stage('Run Docker Compose File'){
        sh 'sudo docker-compose up -d'
        sh 'sudo docker-compose up -d'
    }
    
    stage('Push Image To Docker Hub'){
        sh 'sudo docker login -u "anil76201" -p "Reddy@0108" docker.io'
        sh 'sudo docker push anil76201/springrest:v1'
    }
}
