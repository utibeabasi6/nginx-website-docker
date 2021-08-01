# CI/CD pipeline with github actions

![Docker image](readme_images/docker.png)     ![Docker image](readme_images/github_actions.png)

This project aims to demonstrate how to build a Continous integration pipeline to automatically build and push a docker image to docker hub whenever a push is made to the repository.

## Installation guide
### **Install git**
[http://installgit.com](https://git.com)

### **Install docker**
[http://installdocker.com](https://docker.com)

## Setup
1. Clone the project repository by running:
    ```
    git clone <REPO_URL> 
    ```
    ![language](readme_images/git-clone.png)

2. Navigate to the nginx-website folder by running:
    ```
        cd nginx-website-docker
    ```

3. Build the docker image by running:
    ```
        docker build -t <your_username>/nginx-website:latest .
    ```
    ![alt](readme_images/docker-build.png)

    > Note: this assumes the Dockerfile is in the directory you are running this command

4. Run the newly built image to check out the website in a browser
    ```
        docker run -p 80:80 <your_username>/nginx-website
    ```
    ![git-clone](readme_images/docker-run.png)

    This creates a new container from the image and binds port 80 of the container to port 80 of the host machine

5. Visit `http://localhost` to view the website

    ![website](readme_images/website.png)

    Click `ctrl+c` to stop the running container

## Github actions
### What is github actions? 
GitHub Actions makes it easy to automate all your software workflows, now with world-class CI/CD. Build, test, and deploy your code right from GitHub. Make code reviews, branch management, and issue triaging work the way you want.

### Getting started with github actions

[https://docs.github.com/actions](https://docs.github.com/actions)

## A look at our pipeline

