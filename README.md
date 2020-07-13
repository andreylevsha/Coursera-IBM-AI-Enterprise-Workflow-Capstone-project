# IBM AI Enterprise Workflow Capstone
Solution for the IBM AI Enterprise Workflow Capstone project.

Please, go to [https://github.com/aavail/ai-workflow-capstone](https://github.com/aavail/ai-workflow-capstone) to read the project description and deliverables.

All commands are from this directory.

## Parts 1 & 2
Please refer to the notebook `analysis.ipynb` to get detailed insights. 
### Data Ingestion
To run the data ingestion script
```bash
$ python data_ingestion.py
```

### Data Visualization
To run the data visualization script
```bash
$ python data_visualization.py
```
All images created are saved in the *images* sub-directory.


### Data Engineering
To run the data ingestion script
```bash
$ python data_ingestion.py
```

### Modelling
To run the modelling script
```bash
$ python modelling.py
```
The models are saved as joblib files in the *models* sub-directory.


### Test the flask API

From the project directory start the app:

```bash
$ python app.py
```

Then go to [http://localhost:8080/](http://localhost:8080/)

### Unit Tests
The unit tests for the Model, API and Logs are created as package **unittests**. You can access the code in the sub-directory *unittests*.

From the project directory run Unit Tests with a single script

```bash
$ python run-tests.py
```

### Docker Container
**Build the Docker image and run it**

Step one: build the image (from the directory that was created with this notebook)
 
```bash
$ docker build -t capstone-ml-app .
```

Check that the image is there.

```bash
$ docker image ls
```

You may notice images that you no longer use.  You may delete them with

```bash
$ docker image rm IMAGE_ID_OR_NAME
```

Run the container

```bash
$ docker run -p 4000:8080 capstone-ml-app
```

Test the running app

First go to [http://localhost:4000/](http://localhost:4000/) to ensure the app is running and accessible.

### Post Production Analysis
To run the perfomance monitoring script
```bash
$ python monitoring.py
```
