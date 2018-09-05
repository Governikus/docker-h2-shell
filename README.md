# docker-h2-shell

Docker image to use the h2 shell to connect to h2 databases

## Usage

Stop the eIDAS Middleware container before running this container.

```
docker run --rm -it -v eidas-database:/eidas governikus/docker-h2-shell -url jdbc:h2:/eidas/eidasmw -user [YOUR SQL USERNAME] -password [YOUR SQL PASSWORD] -sql '[YOUR SQL STATEMENT]'
```
The values for username and password can be taken from the application.properties.

Example:
```
docker run --rm -it -v eidas-database:/eidas governikus/docker-h2-shell -url jdbc:h2:/eidas/eidasmw -user sa -password sa -sql 'select * from PENDINGCERTIFICATEREQUEST;'
```
