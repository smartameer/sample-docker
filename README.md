Docker Test
---

Sample App for docker using python and redis for visit count


### installation
- make sure 8099 port open
- Run these commands
```
docker-compose -f docker-compose.yml build
docker-compose -f docker-compose.yml up -d
```

- Now open browser with http://localhost:8099
- On reload visits count will increase

- Turning off
```
docker-compose -f docker-compose.test.yml down
```


### Testing installation
- Run these commands
```
docker-compose -f docker-compose.test.yml build
docker-compose -f docker-compose.test.yml -p app up -d
```

- Testing status

```
docker wait app_test_1  // status of app testing
docker logs -f app_test_1  // for checking logs of testing
```

- Turning off
```
docker-compose -f docker-compose.test.yml -p app down
```


### useful commands

```
docker images //check which images are installed
docker ps -a   // check which processes are active
docker rmi <imageid> // removing unused image

```
