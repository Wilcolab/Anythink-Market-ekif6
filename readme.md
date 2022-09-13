# Welcome to the Anythink Market repo

To start the app use Docker. It will start both frontend and backend, including all the relevant dependencies, and the db.

Please find more info about each part in the relevant Readme file ([frontend](frontend/readme.md) and [backend](backend/README.md)).

## Development

When implementing a new feature or fixing a bug, please create a new pull request against `main` from a feature/bug branch and add `@vanessa-cooper` as reviewer.

## First setup

### Dependencies:

* [Docker](https://docs.docker.com/engine/install/)
* [Docker-compose](https://docs.docker.com/compose/install/)

The above are required to run the service locally. Please install with the guidance listed in the link.

Please verify the installation is working by running the following cmds:

```
docker -v  
Docker version 20.10.17, build 100c701
```

```
docker-compose -v
Docker Compose version 2.10.2
```

**NOTE: The version may change**



### Installation

To run the service locally first we need to clone the environment locally. Please move to the directory where you want to place the repository and run:

```
git clone https://github.com/ObelusFamily/Anythink-Market-ekif6.git
```

Once that is complete please run the following to verify that you can run the service locally.

```
docker-compose up
```

If everything has worked out you should see the three containers running:

```
docker ps 
CONTAINER ID   IMAGE                                           COMMAND                  CREATED          STATUS          PORTS                      NAMES
f7a82bfa5275   anythink-market-ekif6-anythink-backend-node     "docker-entrypoint.s…"   27 minutes ago   Up 27 minutes   0.0.0.0:3000->3000/tcp     anythink-backend-node
fdb5df83ca78   anythink-market-ekif6-anythink-frontend-react   "docker-entrypoint.s…"   27 minutes ago   Up 27 minutes   0.0.0.0:3001->3001/tcp     anythink-frontend-react
37337dfb0aa0   mongo                       
```

As well as the message:

```
You can now view anythink-market-front in the browser.

  Local:            http://localhost:3001
  On Your Network:  http://172.18.0.3:3001

Note that the development build is not optimized.
To create a production build, use yarn build.

```

At this point you double check the server by going to [Ping](http://localhost:3000/api/ping) and verify you see: 

```
{"msg":"Pong! Seems like Everythink is working, great job!"}
```



### Congratz you setup the project!