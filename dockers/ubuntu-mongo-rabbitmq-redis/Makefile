NAME=ubuntu_mongo_rabbitmq_redis

build:
	docker build -t $(NAME) .

run:
	docker run -i -t -p 27017:27017 -p 5672:5672 -p 6379:6379 --name test_$(NAME) $(NAME)

stop:
	docker stop test_$(NAME)

rm:
	docker rm test_$(NAME)

clean:
	docker stop test_$(NAME)
	docker rm test_$(NAME)
	docker rmi $(NAME)

.PHONY: run clean
