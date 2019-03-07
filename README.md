Docker for Rails
3/06, Wed
pg81



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
docker-compose run --rm database psql -U postgres -h database
docker-compose up logs -f database
docker-compose up logs -f web
mkdir -p .env/development, pg77
docker-compose run --rm web bin/rails db:create, pg78
docker-compose up -d --force-recreate web   --recreate container web
docker-compose exec web bin/rails g scaffold User first_name:string last_name:string, pg80
docker-compose exec web bin/rails db:migrate
http://localhost:3000/users
