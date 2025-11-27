## How to setup

cd docker-dfir-elk

docker compose up -d

Use https://github.com/dfirvault/CSV2ELK to import data
python3 -m venv venv-dfir-elk
source venv-dfir-elk/bin/activate
pip install pandas requests tqdm
git clone https://github.com/dfirvault/CSV2ELK.git

http://localhost:5601/app/home

Create a new data view for your data