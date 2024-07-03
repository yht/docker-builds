all: pull install

install:
	docker build . -t ryht/debian-python:bookworm
	docker tag ryht/debian-python:bookworm ryht/debian-python:12
	docker push ryht/debian-python:bookworm
	docker push ryht/debian-python:12

pull:
	docker pull ryht/debian:bookworm