Docker for Rails
1/24, Thurs



docker-compose up
docker build -t docker_rails .
docker run -p 3000:3000 docker_rails rails s -b 0.0.0.0

