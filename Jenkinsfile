node {
   echo 'Hello World'
   sh "docker-compose --project-name microgateway \
                 --file mg/get-started/docker-compose/docker-compose.yml \
                 --file mg/get-started/docker-compose/docker-compose.db.consul.yml \
                 --file mg/get-started/docker-compose/docker-compose.lb.dockercloud.yml \
                 up -d --build"
}
