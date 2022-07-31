Hello if you want tu run application you need clone project


git clone 

nex step cd folder project


cd DockerFile

and need build project with your example name 


<b>docker build -t example name .</b>



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

if you want to run new Ubuntu image you need rename file DockerFilenew -> DockerFile
and old DockerFile->DockerFile_old

<b>
mv dockerfile dockerfile_old
mv DockerFilenew dockerfile

</b>

after that you can use previously steps (build/run project)

when you get message

Successfully built **********
Successfully tagged example name:latest


you can run project (you can change ports and name) with name you build image
<br><b>docker run -d -p 98:80  --name=nginx --restart=always  example name</b>

docker ps -a


you can see docker status running container with you example name

after that you can open ip your server + port 98 and you can get web page 

and you can check os release in docker container 

docker exec -it example name(or id container) /bin/bash
