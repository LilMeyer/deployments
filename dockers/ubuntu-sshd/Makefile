
build:
	cp ~/.ssh/id_rsa.pub id_rsa.pub
	docker build -t ubuntu_sshd .

run:
	docker run -d -p 32782:22 --name test_ubuntu_sshd ubuntu_sshd

stop:
	docker stop test_ubuntu_sshd

rm:
	docker rm test_ubuntu_sshd

ssh:
	ssh root@localhost -p 32782

clean:
	docker stop test_ubuntu_sshd
	docker rm test_ubuntu_sshd
	docker rmi ubuntu_sshd

.PHONY: run clean
