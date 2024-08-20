all: pulls build push

build:
	docker build . -t ryht/yolo7-notebook
push:
	docker push ryht/yolo7-notebook

pulls:
	docker pull quay.io/jupyter/pytorch-notebook
