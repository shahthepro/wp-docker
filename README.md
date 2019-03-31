# wp-docker
Nginx reverse proxy with multiple wordpress containers and redis container.

## Running Containers
- Update `nginx/nginx.conf` to add your server names.
- Change database passwords in `db/setupDB.sql` and `docker-compose.yml`
- And then
  ```
  $ docker-compose up -d
  ```

### Permission fix
After container has been started, to fix wordpress permissions issues
```
$ chown -R 1000:1000 html/wordpress_1
$ chown -R 1000:1000 html/wordpress_2
```

## TODO
[] Move database names, usernames and passwords to environment file
