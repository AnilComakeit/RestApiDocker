node{
    stage('SCM Checkout'){
        sh 'echo "started"'
        git branch: 'main', url: 'https://github.com/AnilComakeit/RestApiDocker'
        sh 'echo "Done!!!!"'


        
    }
     stage('Maven Build'){
        sh '  mvn clean'
        sh '  mvn test'
        sh '  mvn install'
    }
    stage('Build App.jar'){  
        sh 'sudo docker build -t app:v1 .'
        
        sh 'echo "Build Done!!!!"'
    }
    
    stage('Run Docker Compose File'){  
        sh 'sudo docker-compose up -d'
        sh 'echo "Docker up!!!!"'
    }
    
    stage('Push Image To Docker Hub'){
        sh 'sudo docker login -u "anil76201" -p "Reddy@0108" docker.io'
    
        sh 'sudo docker push anil76201/app:v1'
    }
}
