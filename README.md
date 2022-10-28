# teste-bytebase

   ```bash
   docker run --init \
  --name bytebase \
  --restart always \
  --publish 5678:8080 \
  --health-cmd "curl --fail http://localhost:5678/healthz || exit 1" \
  --health-interval 5m \
  --health-timeout 60s \
  --volume ~/.bytebase/data:/var/opt/bytebase \
  bytebase/bytebase:1.7.0 \
  --data /var/opt/bytebase \
  --port 8080 \
  --external-url http://localhost:5678
   ```

   ```bash
 docker run --name mysqld \
  --publish 3306:3306 \
  -e MYSQL_ROOT_HOST=172.17.0.1 \
  -e MYSQL_ROOT_PASSWORD=testpwd1 \
  mysql/mysql-server:8.0

   ```
