#local-mobile-gateway

## Create an API gateway to route traffic from virtual devices to different servers depending on the route


## Steps to configure the service

### Run the docker compose

```sh
 docker-compose up -d
```


### Configure the certificate
- Copy the cert nginx-selfsigne2.crt inside the android (drag and drop)
- Install the cert  `Setting app -> Security -> Encryption & Credentials -> Install a Certificate -> Select CA Certificate option`
- Select Install Anyway
- Select the Certificate that you downloaded on your storage


### Configure the app to use the proxy

Using the default configuration the https route will be `https://10.0.2.2:8090/`


### Adapt the routes

To adapt the routes you will need to modify the file `nginx\conf.d\service.conf`
and restart the docker instance.
