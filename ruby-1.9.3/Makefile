main: build
.PHONY: build bash live

build:
	sudo docker build -t jumski/ruby-1.9.3 .

bash:
	sudo docker run -it --rm jumski/ruby-1.9.3 bash

live:
	echo Dockerfile | entr -r make
