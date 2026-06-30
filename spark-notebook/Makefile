all: build push

build:
	docker build . -t ryht/spark-notebook:3.5.0
push:
	docker push ryht/spark-notebook:3.5.0

pulls:
	docker pull quay.io/jupyter/all-spark-notebook
