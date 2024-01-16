setup:
	python -m venv ~/.udacity-devops 
	~\.udacity-devops\Scripts\activate

install:
	python -m ensurepip
	python.exe -m pip install --upgrade pip
	pip install -r requirements.txt

test:
	#python -m pytest -vv --cov=myrepolib tests/*.py
	#python -m pytest --nbval notebook.ipynb

validate-circleci:
	circleci config process .circleci\config.yml

run-circleci-local:
	circleci local execute

lint:
	hadolint demos/flask-sklearn-student-starter/Dockerfile
	pylint --disable=R,C,W1203 demos/**/**.py

all: install lint test
