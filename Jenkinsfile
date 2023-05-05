// Go-Docker-EC2
// Write a Jenkinsfile that performs the following actions:
// 1. 'build base image: This stage builds a base Docker image that the application will be built upon.
// 2. Run the make build-base command:  which builds the base Docker image using the Dockerfile located in the base directory of the repository.
// 3. Run the tests:
//   - ‘make build-test'- builds a Docker image that includes the application and its dependencies.
//   -  'make test-unit'- runs the unit tests for the application inside a Docker container.
// 4. List the contents of the current directory for debugging purposes.
// 5. Build the final Docker image that will be used to deploy the application.
//      make build command (builds a Docker image that includes the application and its dependencies)
// 6. Deploy the Go application to an EC2 instance:
//   - Install Docker on the EC2 instance
//   - Copy the application files to the EC2 instance
//   - Build and run the Docker container: Once the application code and Dockerfile are on the EC2 instance, you       can build and run the Docker container using the docker build and docker run commands.
// 7. Slack notifications on pipeline completion/ failure. 
// BONUS:
// Add ‘Push to registry’ stage
// Add ‘Push with latest release tag' stage 
// Add a stage for rolling updates: Modify the deployment stage to use a rolling update strategy when deploying the Docker container to the EC2 instance. This will ensure that the application remains available during the update process.
// HINT: In the 'Rolling Update' stage, we use the docker pull command to update the local copy of the Docker image on the EC2 instance, and then use the docker service update command to perform a rolling update.         --update-parallelism 1 option ensures that only one instance of the application is updated at a time, and the     --update-delay 10s option specifies a delay of 10 seconds between updates. 

pipeline {
    stages {
        stage("Build base image") {
            steps {
                sh "make build-base"
            }
        }
    }
}