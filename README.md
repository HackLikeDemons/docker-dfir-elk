# How to 

In your tools directory, clone this repo into docker-dfir-elk

```BASH 
git clone https://github.com/HackLikeDemons/docker-dfir-elk.git
```

You can start your local local ELK stack, after adding the .env file with:
```BASH 
docker compose up -d
```

## .env file

Add a .env file to your directory and change the password

```YAML
# Password for the 'elastic' user (at least 6 characters)
ELASTIC_PASSWORD=elastic

# Password for the 'kibana_system' user (at least 6 characters)
KIBANA_PASSWORD=elastic

# Version of Elastic products
STACK_VERSION=9.2.1

# Set the cluster name
CLUSTER_NAME=docker-cluster

# Set to 'basic' or 'trial' to automatically start the 30-day trial
LICENSE=basic

# Port to expose Elasticsearch HTTP API to the host
ES_PORT=9200

# Port to expose Kibana to the host
KIBANA_PORT=5601

# Increase or decrease based on the available host memory (in bytes)
MEM_LIMIT=2147483648    # 2147483648 Byte = 2GB
```

## Importing CSV data

If you don't want to add more tools to your pipeline, you just use
http://localhost:5601/app/home#/tutorial_directory/fileDataViz
to upload your CSV data and create a data view. This is the easiest way.


You can also use a tool like https://github.com/dfirvault/CSV2ELK to import data.

In your tools directory:
```BASH
python3 -m venv venv-dfir-elk
source venv-dfir-elk/bin/activate
pip install pandas requests tqdm
git clone https://github.com/dfirvault/CSV2ELK.git
cd CSV2ELK
python3 CSV2ELK.py
```

Afterwards create a new data view for your data
http://localhost:5601/app/home
