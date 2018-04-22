# RocketChat Setup

## Installing

## Docker Compose Additional Configuration

* Add port to mongo service

```
port:
  - 27017:27017
```

## Create an acount for mongo authentication

```
sudo docker ps -a
sudo docker run -it <containerID> bash
mongo
use admin
db.createUser({user: "rocket", pwd: "password", roles: [{role: "readWrite", db: "rocketchat"}]})
```
