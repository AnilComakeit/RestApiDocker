node{
    stage('SCM Checkout'){
        sh 'echo "started"'
        sh 'git clone https://github.com/AnilComakeit/RestApiDocker.git'
        sh 'cd RestApiDocker/'


        
    }
     stage('Maven Build'){
        sh '  mvn clean'
        sh '  mvn test'
        sh '  mvn install'
    }
    
    stage('Run Docker Compose File'){  
        sh 'sudo docker-compose up  '
    }
    
    stage('Push Image To Docker Hub'){
        sh 'sudo docker login -u "anil76201" -p "Reddy@0108" docker.io'
        sh 'sudo docker push anil76201/springrest:v1'
    }
}
