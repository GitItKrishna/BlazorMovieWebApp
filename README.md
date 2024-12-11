**Blazor Movie Web App**

**Docker Build:-**
docker build -t blazor-movie-server-with-docker .

**Docker Compose:-**
docker-compose up --build -d  

**Redis Cache** (Including the below entry in the docker-compose.yml and add the Cache entry in the connection string of appsettings.json as below)
moviesRedis:
    image: redis
    ports:
      - "6379:6379"

appsettings.json:-
     "Cache": "moviesRedis:6379"
