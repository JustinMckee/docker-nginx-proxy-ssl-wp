# Nginx Reverse Proxy for Local WP w/ SSL

1. Create directory docker/certs.
2. In certs directory, use openssl to generate key and certificate [Instructions](https://docs.docker.com/engine/swarm/configs/#advanced-example-use-configs-with-a-nginx-service) - Hint: Chrome does not recognize Common Name so Alternative names has to be added.
3. Update path to certificate and certificate key from within docker/nginx/nginx.conf
4. Optionally change WORDPRESS_CONFIG_EXTRA in docker-compose.yml & your server_name in nginx.conf
5. Run docker-compose up. If you need to rebuild add the --build flag. 
