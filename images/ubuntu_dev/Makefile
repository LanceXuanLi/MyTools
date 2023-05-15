
LOCAL_PATH=/Users/nanxuanli/work/work
export LOCAL_PATH

CONTAINER_PATH=/work
export CONTAINER_PATH

build:
	docker build -t my-ubuntu-dev .

run: 
	docker run -it --name ubuntu-dev -v $(LOCAL_PATH):$(CONTAINER_PATH) my-ubuntu-dev