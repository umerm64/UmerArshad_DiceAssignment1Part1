# UmerArshad_DiceAssignment1Part1
Dockerfile Creation, GitHub and DockerHub Integration

## Step 1
I have selected the following flask application that I am going to containerize using docker.
```python3
from flask import Flask, render_template
import os

app = Flask(__name__)


@app.route('/')
def home():
    return render_template('index.html')


if __name__ == "__main__":
    port = int(os.environ.get('PORT', 5000))
    app.run(debug=True, host='0.0.0.0', port=port)
```

Its a simple python flask application that has a single route `localhost:5000/`

## Step 2
The application required the following dependencies:
* python3
* flask
* Werkzeug==2.0.2


## Step 3
Dockerfile is created and present in the current repository.
The command that is going to run upon creation of this docker is 
`python app.py`

# Step 4
Docker image is built successfully with the command
`docker build -t task1 .`

## Step 5
The docker image is pushed to the dockerhub repository.
It can be obtained from here: https://hub.docker.com/r/umerarshad123/task1

## Step 6
Github repository is created here: https://github.com/umerm64/UmerArshad_DiceAssignment1Part1
