# Run Graphcast to make weather predictions:

0. Add a .cdsapirc file to the folder containing the url and key for the [CDS API](https://cds.climate.copernicus.eu/api-how-to) connection.
1. Set the date of your choice in the prediction.py file (check data is available for this date on the "ERA5 hourly data on single levels from 1940 to present" dataset
2. Build the docker iamge with the dockerfile:

```
docker build -f graphcast.dockerfile -t graphcast .
```

3. Run the docker image using the compose file, creating a container:

```
docker compose -f graphcast.yaml up
```

4. While the docker image is running, open another terminal and enter the docker container:

```
docker exec -it graphcast /bin/bash
```

5. Run the prediction file:

```
python3 prediction.py
```

# Compare predictions to real weather data

Run the plots.ipynb notebook in Colab or locally !
