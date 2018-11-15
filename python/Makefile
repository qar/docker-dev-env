include ./Makefile.variables

build:
	docker build . -t $(DEV_IMAGE) -f ./DockerfileDev

run: build
	docker run --rm -d -v $(shell pwd):/data --name $(DEV_IMAGE) $(DEV_IMAGE)

access:
	docker exec -it $(DEV_IMAGE) sh

stop:
	docker stop $(DEV_IMAGE)
