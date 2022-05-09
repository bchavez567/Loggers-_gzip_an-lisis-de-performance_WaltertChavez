# Dependencias

npm i express

npm i -g artillery

npm start -- 8081

npm start -- 8081 CLUSTER


## ARTILLERY

artillery quick -c 50 -n 40 http://localhost:8081?max=10000 > result_fork.txt

artillery quick -c 50 -n 40 http://localhost:8081?max=10000 > result_cluster.txt

## PROFILING

artillery quick --count 10 -n 50 "http://localhost:8080/auth-bloq?username=marian&password=qwerty123" > result_bloq.txt

## NODE INSPECT

node --inspect index.js


## Node built-in profiler

Con el siguiente comando, creamos un nuevo usuario:
curl -X GET "http://localhost:8080/newUser?username=marian&password=qwerty123"

Ahora, puedo usar el test de carga. Para eso, utilizo el siguiente comando:

artillery quick --count 10 -n 50 "http://localhost:8080/auth-bloq?username=marian&password=qwerty123" > result_bloq.txt


