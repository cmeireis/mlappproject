Deploying a pre-trained, sklearn model that has been trained to predict housing prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on.
You can read more about the data, which was initially taken from Kaggle, on the data source site.
This project tests your ability to operationalize a Python flask app—in a provided file, app.py—that serves out predictions (inference) about housing prices through API calls. 
This project could be extended to any pre-trained machine learning model, such as those for image recognition and data labeling.

# Setup the Environment
1. Create a virtualenv and activate it
2. Run make install to install the necessary dependencies
- Running app.py
1. To test the app run from command line: python app.py
2. Run in Docker: ./run_docker.sh
3. Deploy to Docker repository: ./upload_docker.sh
4. Run in Kubernetes: ./run_kubernetes.sh
- Kubernetes Steps
1. Setup and Configure Docker locally
2. Setup and Configure Kubernetes locally
3. Create Flask app in Container
4. Run via kubectl
# Repository files
- app.py contacts sklearn model as described above in introduction.
- Dockerfile includes items for docker container.
- Makefile defines a set of tasks to be executed.
- requirements.txt is the file that defines the python package requirements to run this project.
- run_docker.sh is used to build the docker container for this project.
- upload_docker.sh is used to upload docker container built localy to docker repository.
- make_prediction.sh is used to load data into app.py to produce results.
- run_kubernetes.sh is used to deploy container to a kubernetes pod.
- docker_out.txt includes output results from running make_prediction.sh in separate terminal window.
- kubernetes.out.txt shows output from when running make_prediction.sh after deployed to kubernetes.
