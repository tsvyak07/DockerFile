Hello if you want tu run application you need clone project


<b>git clone </b>

nex step cd folder project


<b>cd DockerFile</b>

and need build project with your example name 


<b>docker build -t [Name Of the Image]  .</b>



when you get message 

Successfully built **********
Successfully tagged example name:latest

but you need check new image (you can see last image with you example name)

<b>docker images</b>

you can run project (you can change ports and name) with name you build image
<br><b>docker run -d -p 88:80  --name=nginx --restart=always  example name</b>

docker ps -a


you can see docker status running container with you example name

after that you can open ip your server + port 88 and you can get web page 

if you want to run new Ubuntu image you need rename file
DockerFile->DockerFile_old
DockerFilenew -> DockerFile
 

<b>
mv dockerfile dockerfile_old
mv DockerFilenew dockerfile

</b>

after that you can use previously steps (build/run project)
docker build -t [Name Of the Image]  .
when you get message

Successfully built **********
Successfully tagged example name:latest


you can run project (you can change ports and name) with name you build image
<br><b>docker run -d -p 98:80  --name=nginx --restart=always  example name</b>

<b>docker ps -a</b>


you can see docker status running container with you example name

after that you can open ip your server + port 98 and you can get web page 

and you can check os release in docker container 

<br><b>docker exec -it example name(or id container) /bin/bash</b>

run command 
cat /etc/os-release

you can see you version os Ubuntu

try run mc app or htop app 
_________________________________________________________________________________


How to run Docker Tomcat

fist step you need rename 


DockerFile->DockerFile_old
DockerFileTomcat -> DockerFile

<b>
mv dockerfile dockerfile_old
mv DockerFileTomcat dockerfile
</b>

after that you can use previously steps (build/run project)
docker build -t [Name Of the Image]  .

you can run project (you can change ports and name) with name you build image

<b>docker container run -it -d --name tomcatcontainer1 -p 8081:8080 [Name Of the Image]</b> 


<b>docker ps -a</b>
you can see docker status running container with you example name


after that you can open in your web browser http://ip server:8081/SampleWebApp


This test srv with Tomcat and default JDK 

-------------------------------------------------------------------------------------

Last project this File DockerFileMVTC (Tomcat +default JDK +Naven + boxfuse-sample )


DockerFile->DockerFile_old
DockerFileTomcat -> DockerFile

<b>
mv dockerfile dockerfile_old
mv DockerFileMVTC dockerfile
</b>

after that you can use previously steps (build/run project)

docker build -t [Name Of the Image]  .

when build finished you can check result

<b>docker images</b>

you can run project (you can change ports and name) with name you build image

<b>docker container run -it -d --name tomcatcontainer2 -p 8082:8080 [Name Of the Image]</b>

<b>docker ps -a</b>

you can see docker status running container with you example name


after that you can open in your web browser http://ip server:8082/hello-1.0/