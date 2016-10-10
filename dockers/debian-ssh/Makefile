
NAME=debian_ssd
PORT=32783

build:
	docker build -t $(NAME) .

run:
	docker run -d -p 32783:22 --name $(NAME) $(NAME)

start:
	docker start $(NAME)

stop:
	docker stop $(NAME)

rm:
	docker rm $(NAME)

ssh:
	ssh root@localhost -p 32783

clean:
	docker stop $(NAME)
	docker rm $(NAME)
	docker rmi $(NAME)

.PHONY: run clean
