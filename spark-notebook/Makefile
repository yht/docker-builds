all: pull build push

build:
	docker build . -t ryht/spark-notebook:3.5.2
push:
	docker push ryht/spark-notebook:3.5.2
pull:
	docker pull quay.io/jupyter/all-spark-notebook:spark-3.5.2
