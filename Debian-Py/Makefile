all: pull install push

install:
	docker build . -t ryht/debian-python:bookworm

pull:
	docker pull ryht/debian:bookworm

push:
	docker tag ryht/debian-python:bookworm ryht/debian-python:12
	docker push ryht/debian-python:bookworm
	docker push ryht/debian-python:12

