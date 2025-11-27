## How to setup

clone this repo into docker-dfir-elk

git clone https://github.com/HackLikeDemons/docker-dfir-elk.git

cd docker-dfir-elk

docker compose up -d

## Importing CSV data
To import CSV data as easy as possible, we will use https://github.com/dfirvault/CSV2ELK to import data

In your tools directory:
python3 -m venv venv-dfir-elk
source venv-dfir-elk/bin/activate
pip install pandas requests tqdm
git clone https://github.com/dfirvault/CSV2ELK.git
cd CSV2ELK
python3 CSV2ELK.py

http://localhost:5601/app/home

Create a new data view for your data