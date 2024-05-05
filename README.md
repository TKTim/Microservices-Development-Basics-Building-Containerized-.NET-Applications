# Microservices-Development-Basics-Building-Containerized-.NET-Applications

url: https://www.udemy.com/course/dotnet-docker/learn/lecture/14975356#content

## docker commands
```

```
![alt text](image.png)

## docker IIS
### docker IIS install and start
```
1. use docker to pull <Windows IIS>
2. docker run -d -p <from_port:to_port> <iis_image> {ex: docker run -d -p 80:80 mcr.microsoft.com/windows/servercore/iis:windowsservercore-ltsc2019}
3. search localhost on browser and you should see the following pic.
```
![alt text](image-1.png)
### alter file in container
```
* To get in a container
1. docker exec -it <TED> cmd {ex: docker exec -it 4d9 cmd}
```
![alt text](image-2.png)
```
* IIS default directory
1. cd /inetpub/wwwroot
2. del *
3. echo "Hello World Tim" > index.html
4. refresh browser
```
![alt text](image-3.png)

### stop and create new image
```
1. docker stop 4d9
* After stop it, use docker ps -a to show all the container
2. docker commit 4d9 myapp1
```
![alt text](image-6.png)
![docker](image-4.png)

## Dockerfile
### start and run
![alt text](image-7.png)
```
1. create a file called "Dockerfile"
2. edit the file like below.
3. docker build -t <image>
* It will automatically run the file called "Dockerfile", so be sure the filename is correct.
```
![alt text](image-8.png)
![alt text](image-9.png)
### Appendix
![alt text](image-10.png)
![alt text](image-11.png)
![alt text](image-12.png)
![alt text](image-13.png)
### IIS Support https connect
url: https://learn.microsoft.com/en-us/virtualization/windowscontainers/samples?tabs=Application-frameworks

## Publish to Dockerhub and Azure Container Registry

### DockerHub
```
1. docker login
2. docker tag <image_name> <user_name/files_name:version>
3. docker push <image_name>
Docker 取出
* docker pull
```
![alt text](image-14.png)

### Azure Container Registry
![alt text](image-15.png)
![alt text](image-16.png)
```
Use the information to login
1. Docker login <Login_Server>
2. The commands are the same as dockerhub
```

## Deploy .NET in Container
![alt text](image-17.png)
### Run with mount directory
![alt text](image-18.png)
### Publish to Azure
![alt text](image-19.png)
![alt text](image-20.png)
```
Add new service - Web App
```
![alt text](image-21.png)
![alt text](image-22.png)