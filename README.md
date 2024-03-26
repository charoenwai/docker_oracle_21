# docker_oracle_21

# build image
- docker build -t oracle-db-21c -f Dockerfile.xe .

# run docker container
- docker run --name Oracle21 -p 1521:1521 -p 5500:5500 -e ORACLE_PWD=training2024 -e ORACLE_CHARACTERSET=utf8 -d oracle-db-21c
- docker exec -it Oracle21 sqlplus system/training2024@1521:1521/XE
