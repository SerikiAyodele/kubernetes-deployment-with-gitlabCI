#### demo - Deploying with Gitlab-CI

This demo app shows a simple user profile app set up using 
- index.html with pure js and css styles
- nodejs backend with express module
- mongodb for data storage

Components are:
- Docker and Docker-Compose
- Kubernetes
- Gitlab-CI

### With Docker And Docker-Compose

Step 1: Prepare docker file

Step 2: Build  docker image from application 
    docker build -t my-app:1.0 . 

Step 3: Push the application image to created docker repository
    docker push my-app:1.0 

Step 4: Reference the build in the docker compose file

Step 5: start mongodb and mongo-express

    docker-compose -f docker-compose.yaml up
    
    _You can access the mongo-express under localhost:8080 from your browser_
    
Step 6: in mongo-express UI - create a new database "my-db"

Step 7: in mongo-express UI - create a new collection "users" in the database "my-db"       
    
Step 5: access the nodejs application from browser 

    http://localhost:3000

   
### With Kubernetes
Step 1: Deploy yaml files
    Kubernetes applt -f kustomization.yaml

### With Gitlab-CI
Once the code is commited to gitlab, a pipeline will be automatically triggered
