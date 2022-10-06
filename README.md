## Final Project DevOps using Docker

![images](https://user-images.githubusercontent.com/23287190/194307350-8c80e1f0-3a70-4d24-b36c-7646c0d55271.jpeg)

how to start?

1. clone `https://github.com/mrzdtydlntm/project-akhir-sanbercode` follows all the steps

2. Setup docker-compose.yaml, nginx conf, db mounting volume, 
```bash
# run docker compose
sudo docker compose up -d --build

# see docker compose container
sudo docker compose ps -a

# see logs
sudo docker compose logs -f <container compose>

# maint
sudo docker compose down
sudo docker compos restart
```

3. explore it! or can try to hit some endpoints.
```bash
# rest create a new record for table_user
curl --location --request POST 'http://localhost:80/register' \
--header 'Content-Type: application/json' \
--data-raw '{
    "email": "muhamadalfarisy@gmail.com",
    "password": "password",
    "firstname": "faris",
    "lastname": "ganteng"
}'
```

```bash
# login with existing record
curl --location --request POST 'http://localhost:80/login' \
--header 'Content-Type: application/json' \
--data-raw '{
    "email": "muhamadalfarisy@gmail.com",
    "password": "password"
}'
```
