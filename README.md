Docker for Rails
1/28, Mon
pg75



docker-compose up
docker build -t docker_rails .
docker run -p 3000:3000 docker_rails rails s -b 0.0.0.0
docker-compose logs -f web
docker-compose build web #rebuilding image
docker run --name redis-container redis
docker-compose run --rm redis redis-cli -h redis #connects to redis cli 
docker-compose stop
docker-compose ps
docker-compose up -d database
