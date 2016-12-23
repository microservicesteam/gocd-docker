This is the repository which contains the Dockerfiles and supporting scripts for dockerized Go-cd server and client forked from [original repo](https://github.com/gocd/gocd-docker) and customized by adding maven plugin to be able to run maven commands during build.

The images can be found on [docker hub](https://hub.docker.com/u/microservicesteam/) and can be started with the following commands:
##### Server:
`sudo docker run -i -t -p 8153:8153 -p 8154:8154 --name bela microservicesteam/gocd-server`

##### Agent:
`sudo docker run -ti --link bela:go-server microservicesteam/gocd-agent`

If you specify the name attribute on the server and link the agent to it as you can see above, the agent automatically will be registered to the server and can be used to run jobs.
With above mentioned command the server will be available on localhost:8153 address.
