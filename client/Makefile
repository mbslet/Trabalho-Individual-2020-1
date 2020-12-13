build:
	sudo docker-compose build

run:
	sudo docker-compose up -d
	sudo docker-compose run api rake db:create 
	sudo docker-compose run api rake db:migrate 