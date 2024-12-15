**Blazor Movie Web App**

 * This app is to create basic create, edit, update, deletion of movies managed by postgres as db.

*  This includes the Redis cache (to check if the data being served is from the cache. If not present in cache, fetches from the db 
     and pushes to cache for next requests for cache hit).
   
*  This includes pushing and deploying docker image to AWS ECS clusters using task definitions , fargate for serving the web.

**Docker Build:-**
* docker build -t blazor-movie-server-with-docker .

**Docker Compose:-**
* docker-compose up --build -d  

**Redis Cache** 

* (Including the below entry in the docker-compose.yml and add the Cache entry in the connection string of appsettings.json as below)

moviesRedis:
    
    image: redis
    ports:
      - "6379:6379"

* appsettings.json:-
     "Cache": "moviesRedis:6379"
