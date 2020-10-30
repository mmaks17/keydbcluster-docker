#start cluster
docker-compose up -d 


#master of cluster running on 6371 port
#set value to cluster
redis-cli -h 127.0.0.1  -p 6371  set myvalue 500


#next can get from any node
redis-cli -h 127.0.0.1  -p 6371  get myvalue 
redis-cli -h 127.0.0.1  -p 6372  get myvalue
redis-cli -h 127.0.0.1  -p 6372  get myvalue