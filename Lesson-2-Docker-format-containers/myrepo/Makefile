setup:
	python -m venv ~/.myrepo
	~\.myrepo\Scripts\activate
	
install:
	python -m ensurepip
	python.exe -m pip install --upgrade pip
	pip install -r requirements.txt

test:
	python -m pytest -vv --cov=myrepolib tests/*.py
	python -m pytest --nbval notebook.ipynb


lint:
	pylint --disable=R,C myrepolib cli web

all: install lint test
