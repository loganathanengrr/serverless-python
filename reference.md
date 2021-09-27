## Run

```
docker build -t serverless-python -f Dockerfile .

docker run -it -p 80:5000 serverless-python

docker run --env PORT=5000 -it -p  80:5000 serverless-python

```

## Push
#### through Docker

```
docker build -t serverless-python -f Dockerfile .

docker tag serverless-python asia.gcr.io/charged-hub-312315/serverless-python

docker push asia.gcr.io/charged-hub-312315/serverless-python
```

#### throuh GCloud


```
gcloud builds submit --tag asia.gcr.io/charged-hub-312315/serverless-python-2 .

```

## Deploy

```
gcloud run deploy serverless-python --image asia.gcr.io/charged-hub-312315/serverless-python --platform managed --region us-west1

```