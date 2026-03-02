#### Installation on MacOs m1 processor by docker

```bash
docker run -d --name weaviate \
  -p 8081:8080 \
  -e QUERY_DEFAULTS_LIMIT=20 \
  -e AUTHENTICATION_ANONYMOUS_ACCESS_ENABLED=true \
  -e PERSISTENCE_DATA_PATH=/var/lib/weaviate \
  -v $(pwd)/weaviate-data:/var/lib/weaviate \
  semitechnologies/weaviate:latest
  ```
  - In this case, the host port is 8081, but inside Docker it still listens on 8080.

` Access via: `http://localhost:8081`.


