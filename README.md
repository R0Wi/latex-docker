# latex-docker
Docker container for building latex documents

Inspired by https://github.com/blang/latex-docker

## Run

### Makefile
If you have a valid `Makefile` for building your latex document, just add another target like
```
docker:
	@echo "Starting docker container for build"
	docker run -v $(CURDIR):/data -it --rm r0wi/latex-docker:main make

```
then run `make docker`.

### Commandline
If you prefer building by command line use a command like this
```
docker run -v $(pwd):/data -it --rm r0wi/latex-docker:main "pdflatex -output-directory . " 
```
or whatever your build command looks like.
