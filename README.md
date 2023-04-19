# Running Keycloak in docker container and connect to mssql

# Running in Local:

#docker-compose up -d

+ login keycloak: 

id: admin 

pass: admin

+ login mssql-db

db: sa 

pass : P@ss@12345

# Running in Linux: 

#docker-compose up -d 

# fix error HTTPS require: 

#docker exec -it {contaierID} bash

cd /opt/jboss/keycloak/bin

$ ./kcadm.sh config credentials --server http://localhost:8080/auth --realm master --user admin

$ ./kcadm.sh update realms/master -s sslRequired=NONE