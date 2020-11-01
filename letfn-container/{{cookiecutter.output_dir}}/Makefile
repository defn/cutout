SHELL := /bin/bash

menu:
	@perl -ne 'printf("%10s: %s\n","$$1","$$2") if m{^([\w+-]+):[^#]+#\s(.+)$$}' Makefile

build: # Build {{ cookiecutter.repo_name }}
	@echo
	docker build -t {{ cookiecutter.repo_name }} .
	docker push {{ cookiecutter.repo_name }}

push: # Push {{ cookiecutter.repo_name }}
	docker push {{ cookiecutter.repo_name }}

bash: # Run bash shell with {{ cookiecutter.repo_name }}
	docker run --rm -ti --entrypoint bash {{ cookiecutter.repo_name }}
