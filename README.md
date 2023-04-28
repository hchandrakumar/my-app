Problem Statement:
The task is to build and deploy an application on bare metal, containerize the application, deploy the container onto the infrastructure of your choice, and document the solution and config on GitHub.

Requirements:

Application:
The application should be built using Python.
The application must have an endpoint that outputs "Hello World".
Containerized Application
The containerized application must run on port 8080.
The containerized application must have an endpoint that outputs "Hello World".

Deploy Container:
Publish the URL of your app(s) for us to test that you have met the requirements.
Document the solution and config on GitHub.
The documentation should describe all steps taken to achieve the above.
Document your thought process and explain your decision-making process.
All config/code should be in the Git repository.

Solution:

To meet the above requirements, we will follow the below steps:

Build the Python application with an endpoint that outputs "Hello World".
Containerize the application using Docker and ensure that it runs on port 8080.
Deploy the container onto the infrastructure of your choice.
Publish the URL of your application for testing.
Document the solution and configuration on GitHub.

Building the Python application:
To meet the requirements, we need to build a simple Python application with an endpoint that outputs "Hello World". We can create a Python file called 'app.py'. This code uses Flask, a popular Python web framework, to create a web application with a single endpoint that returns the string "Hello World!". The application listens on port 8080.

Containerizing the application:
To containerize the Python application, we need to create a Dockerfile that defines how to build the Docker image. Create a file named Dockerfile in the root directory of your application. This Dockerfile uses a Python 3.9 base image, sets the working directory to /app, copies the application code to the container, installs dependencies from a 'requirements.txt' file, exposes port 8080, and starts the application using the 'python app.py' command.

Deploying the container:
To deploy the container, you can choose any infrastructure provider that supports Docker containers, such as Amazon Web Services (AWS), Google Cloud Platform (GCP), or Microsoft Azure. For this example, we will deploy the container on a local machine using Docker.

To build the Docker image, open a terminal in the root directory of your application and run the following command:
docker build -t my-app .

This command will create a Docker image with the name "my-app" using the Dockerfile in the current directory.

To run the Docker container, use the following command:
docker run -p 8080:8080 my-app

This command maps port 8080 on the host to port 8080 in the container and starts the Docker container using the "my-app" image.

Publishing the URL of the application:
To test that the application meets the requirements, you can open a web browser and navigate to http://localhost:8080. You should see the "Hello World" output.

To publish the URL of the application, you can deploy the container to a cloud provider that supports container orchestration, such as AWS Elastic Container Service (ECS) or Google Kubernetes Engine (GKE). Once you have deployed the container, you can obtain the public URL of the container and share it for testing.

Documenting the solution and config on GitHub:
To document your solution and configuration on GitHub, create a new repository and push the code and Dockerfile to the repository. Include a README file that explains the steps you followed to meet the requirements and any relevant information about your infrastructure and deployment. You can also include screenshots or diagrams to help illustrate your solution.

In addition, you should include any configuration files or scripts necessary to deploy the container to your chosen infrastructure provider. This will help others reproduce your deployment and understand how your infrastructure is set up.

Conclusion:
In this README, we have described how to build and deploy a Python application on bare metal, containerize the application using Docker, deploy the container to a cloud provider, and document the solution and configuration on GitHub. By following these steps, you can meet the requirements of the task and create a reproducible and scalable deployment of your Python application.