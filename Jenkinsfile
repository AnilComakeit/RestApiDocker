node{
    stage('SCM Checkout'){
        sh 'echo "started"'
    }
    stage('Run Docker Compose File'){
        
        sh 'sudo docker-compose up -d'
    }
    
    stage('Push Image To Docker Hub'){
        sh 'sudo docker login -u "anil76201" -p "Reddy@0108" docker.io'
        sh 'sudo docker push anil76201/springrest:v1'
    }
}
