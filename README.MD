Hello if you want tu run application you need clone project


git clone 

nex step cd folder project


cd DockerFile

and need build project with your example name 


docker build -t example name .



when you get message 

Successfully built **********
Successfully tagged example name:latest



you can run project (you can change ports and name)



docker run -d -p 88:80 example name  --name=nginx --restart=always

