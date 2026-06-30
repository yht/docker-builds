all: pulls build push

build:
	docker build . -t ryht/spark-notebook:4.0.0
push:
	docker push ryht/spark-notebook:4.0.0
pulls:
	docker pull quay.io/jupyter/all-spark-notebook:spark-4.0.0
