all: pulls bookworm clean

bookworm:
	cp Dockerfile.12 Dockerfile
	docker build . -t ryht/debian:bookworm
	docker tag ryht/debian:bookworm ryht/debian:12
	docker push ryht/debian:bookworm
	docker push ryht/debian:12

bullseye:
	cp Dockerfile.11 Dockerfile
	docker build . -t ryht/debian:bullseye
	docker tag ryht/debian:bullseye ryht/debian:11
	docker push ryht/debian:bullseye
	docker push ryht/debian:11

buster:
	cp Dockerfile.10 Dockerfile
	docker build . -t ryht/debian:buster
	docker tag ryht/debian:buster ryht/debian:10
	docker push ryht/debian:buster
	docker push ryht/debian:10

stretch:
	cp Dockerfile.9 Dockerfile
	docker build . -t ryht/debian:stretch
	docker tag ryht/debian:stretch ryht/debian:9
	docker push ryht/debian:stretch
	docker push ryht/debian:9

jessie:
	cp Dockerfile.8 Dockerfile
	docker build . -t ryht/debian:jessie
	docker tag ryht/debian:jessie ryht/debian:8
	docker push ryht/debian:jessie
	docker push ryht/debian:8

clean:
	rm Dockerfile

pulls:
	docker pull debian:sid
	docker pull debian:bookworm
	docker pull debian:bullseye
	docker pull debian:buster
	docker pull debian:stretch
	docker pull debian:jessie
