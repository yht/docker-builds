all: build push

build:
	docker build . -t ryht/spark-notebook:3.3.2
push:
	docker push ryht/spark-notebook:3.3.2
pulls:
	docker pull quay.io/jupyter/all-spark-notebook
