all: pull install push

install:
	docker build . -t ryht/debian-python:13

pull:
	docker pull ryht/debian:13

push:
	docker tag ryht/debian-python:13 ryht/debian-python:trixie
	docker push ryht/debian-python:13
	docker push ryht/debian-python:trixie

