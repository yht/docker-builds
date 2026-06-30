all: build push

build:
	docker build . -t ryht/spark-notebook:3.4.1
push:
	docker push ryht/spark-notebook:3.4.1
pulls:
	docker pull quay.io/jupyter/all-spark-notebook
