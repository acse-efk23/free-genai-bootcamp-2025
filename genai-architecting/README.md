## Chosing a Model

Cohere `command-r` model is selected to be used. The reasons are:
- Cohere has good integration with Pinecone and optimized for retrieval augmented generation.
- The model context length can be maximum 128k which is necessary as we might process large texts.
- Cohere servers are planned to be used for the model rather than local computers.

## Input Guardrails

The portal shouldn't teach bad words. If such a request is made, the model should be able to handle it gracefully.

## Monitoring

The suggested monitoring stack includes:
- Prometheus for metrics
- Loki for logs
- Jaeger for traces
- Grafana for visualization

## Deployment

The suggest platform for deployment is Google Cloud Run. It is easy to deply as it uses Docker containers. For the initial stage of the app, it will be quick to deploy.

## API

FastAPI is suggested for the API. It integrates well with LLM tools as it is written in Python. It is also easy to use and has good documentation.