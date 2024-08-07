all: pulls build push

build:
	docker build . -t ryht/spark-notebook
push:
	docker push ryht/spark-notebook

pulls:
	docker pull quay.io/jupyter/all-spark-notebook
