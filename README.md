# Teamcity dockerized


This is a local teamcity server running a docker on docker agent


## Database:

```
docker run -it --name teamcity-server-instance  \
    -v /home/jesus.lemus/manuals/devops/teamcity/datadir/:/data/teamcity_server/datadir \
    -v /home/jesus.lemus/manuals/devops/teamcity/logsdir/:/opt/teamcity/logs  \
    -p 8080:8111 \
    jetbrains/teamcity-server
```
```
wget https://jdbc.postgresql.org/download/postgresql-42.1.3.jar
docker cp postgresql-42.1.3.jar teamcity_teamcity-server_1:/data/teamcity_server/datadir/lib/jdbc
```
