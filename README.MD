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
<b>docker run -d -p 88:80 example name  --name=nginx --restart=always</b>
