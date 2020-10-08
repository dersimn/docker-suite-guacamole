## Init Database

Generate Database initialization file:

    docker run --rm guacamole/guacamole /opt/guacamole/bin/initdb.sh --mysql > initdb.sql

## Init SSL

Generate self-signed certificate:

    openssl req -x509 -nodes -days 3650 -newkey rsa:2048 -keyout nginx.key -out nginx.crt

Enter for e.g.:

    Country Name (2 letter code) []:DE
    State or Province Name (full name) []:NRW
    Locality Name (eg, city) []:Duesseldorf
    Organization Name (eg, company) []:My Company
    Organizational Unit Name (eg, section) []:My Department
    Common Name (eg, fully qualified host name) []:localhost
    Email Address []:firstname.lastname@example.org

Common Name must match the IP/DNS from where users will access the server.

## Run

Run with:

    docker-compose up -d

Go to <http://localhost>, login with user/password: `guacadmin`.


[nginx_cert]: https://www.digitalocean.com/community/tutorials/how-to-create-a-self-signed-ssl-certificate-for-nginx-in-ubuntu-18-04
[nginx_redirect]: https://serversforhackers.com/c/redirect-http-to-https-nginx
[guacamole_docker]: https://guacamole.apache.org/doc/gug/guacamole-docker.html
[guacamole_proxy]: https://guacamole.apache.org/doc/gug/proxying-guacamole.html