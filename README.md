# Steps:

0. Add a .cdsapirc file to the folder containing the url and key for the [CDS API](https://cds.climate.copernicus.eu/api-how-to) connection.
1. Build the docker iamge with the dockerfile:

```
docker build -f graphcast.dockerfile -t graphcast .
```

2. Run the docker image using the compose file, creating a container:

```
docker compose -f graphcast.yaml up
```

3. While the docker image is running, open another terminal and enter the docker container:

```
docker exec -it graphcast /bin/bash
```

4. Run the prediction file:

```
python3 prediction.py
```
