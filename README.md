# Dockerproject
Below are the steps that we will be going to perform in the process:

1.Install Git and clone the repo of the Node.js application
2.Install Docker
3.Create a Dockerfile
4.Build a Docker image (docker build)
5.Create and run a Docker container (docker run)
6.Access it on browser


## Commands:

1. Install Git and clone the repo of the Node.js application

#### git clone https://github.com/sanjanathamke/Dockerproject.git


2. Now check the version of the docker once and start the docker and check the status of the docker to know if it is running using the below commands :

#### docker -v 
#### systemctl start docker
#### systemctl status docker

3. Create and configure a Dockerfile


Here is the Dockerfile that I have created :

FROM node:16
COPY . .
RUN npm install
EXPOSE 8080
CMD ["node", "index.js"]



4. Build a Docker image

   Use command :

#### docker build . -t app

Use command to see images:

#### docker images

5. Create and run a Docker container
Using the image that has been built we will create a container out of it and run it:

Use the below commands :

#### docker run -d --name nodejs -p 8080:8080 app:latest



Use command :

#### docker ps 


6. Access it

Now you can take the public IP of the machine and port 8080 to access the application.




### To push repository on github

Commands:


#### git init
#### git add .
#### git commit -m 'Added my project'
#### git remote add origin https://github.com/sanjanathamke/Docker.git (url of your git repository)
#### git push -u -f origin main
