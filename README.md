# Get running with TensorFlow

1. Download docker image [*](https://github.com/saiprashanths/dl-docker) which contains all services such as jupyter, tensorflow, tensorboard, numpy, matplotlib.
	```
	docker pull floydhub/dl-docker:cpu
	```
	
2. Start docker container with the shared folder
	```
	docker run -it -p 8888:8888 -p 6006:6006 -v {shared_folder_path} works:/root/sharedfolder floydhub/dl-docker:cpu bash
	```

3. Container will start with a command line, start jupyter notebook. It will be running at `localhost:8888

	```
	jupyter notebook
	```

4. Run Tensorboard
	```
	docker exec a96fc2bce485 tensorboard --logdir="/root/sharedfolder/my_graph"
	```

	docker exec -d {container_id} {command}
	           (detached: run in background)

5. Use `inline` statement with matplotlib in jupyter

	```
	import matplotlib.pyplot as plt
	%matplotlib inline
	```

6. Plot a simple graph 
	```
	plt.plot(x_axis, y_axis, 'o', label='input data')
	plt.show()
	```

---

## Docker Crash Course

1. List running docker containers
	```
	docker ps
	```

2. Terminate a specific container
	```
	docker rm -f {container_id}
	```

3. Run command on a container
	```
	docker exec a96fc2bce485 tensorboard --logdir="/root/sharedfolder/my_graph"
	```

	docker exec -d {container_id} {command}
	           (detached: run in background thread)
