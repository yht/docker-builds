SPARK_VERSION ?= 4.1.2
all: pulls build push

build:
	docker build --rm . -t ryht/spark-notebook:$(SPARK_VERSION) --build-arg SPARK_VERSION=$(SPARK_VERSION)
push:
	docker push ryht/spark-notebook:$(SPARK_VERSION)
pulls:
	docker pull quay.io/jupyter/all-spark-notebook:spark-$(SPARK_VERSION)
