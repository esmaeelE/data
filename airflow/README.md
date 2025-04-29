# Airflow install and run

This way only work for development purpose dont use other than localhost network.
Reverse proxy way not works dont waste time on it.



Grab from [official documentation](https://airflow.apache.org/docs/apache-airflow/stable/howto/docker-compose/index.html)


Installation steps
```
mkdir -p ./dags ./logs ./plugins ./config
echo -e "AIRFLOW_UID=$(id -u)" > .env
docker compose run airflow-cli airflow config list
docker compose up airflow-init
docker compose up -d 
```

Or simply run `./install.sh`


Clean UP

`docker compose down -v`

check
```
./airflow.sh info
```


