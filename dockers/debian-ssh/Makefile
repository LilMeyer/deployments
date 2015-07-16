
NAME=debian_ssd
PORT=32783

build:
	cp ~/.ssh/id_rsa.pub id_rsa.pub
	docker build -t $(NAME) .

run:
	docker run -d -p 32783:22 --name test_$(NAME) $(NAME)

start:
	docker start test_$(NAME)

stop:
	docker stop test_$(NAME)

rm:
	docker rm test_$(NAME)

ssh:
	ssh root@localhost -p 32783

clean:
	docker stop test_$(NAME)
	docker rm test_$(NAME)
	docker rmi $(NAME)

.PHONY: run clean
