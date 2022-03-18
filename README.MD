# Database Initialization Process

## Prerequisites
 * Docker
 * Dynamodb



## Steps
1. use container service to manage databases(create, host and destroy)
2. write compose file to setup database (docker-compose.yml)
3. execute docker and docker-compose command
4. connect to database use command line or GUI tool
5. design database via GUI tool (Database First)

## Scripts

``` bash
# access Dynamodb database host in docker via terminal
docker exec -it local_dynamodb_dev sh

#check table with aws cli(or you can connect via nosql workbench)
aws dynamodb list-tables --endpoint-url http://localhost:8000

#notice: -sharedDb -dbPath [path] should be enable, or you will get empty array
```

## References
1. [aws doc](https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/DynamoDBLocal.DownloadingAndRunning.html)
2. [dynamo local on mac](https://felixgondwe.medium.com/local-dynamodb-usingdocker-on-mac-62d14cd94fe)
3. [persist local docker volume issues for dynamodb](https://stackoverflow.com/questions/67533058/persist-local-dynamodb-data-in-volumes-lack-permission-unable-to-open-databa)
