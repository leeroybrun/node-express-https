# node-express-https

Example of using Express &amp; Node.js with HTTPS.

## Generation of SSL keys

Create the private key :

```shell
openssl genrsa -out key.pem 1024
```

Create the "Certificate Signing Request" :

```shell
openssl req -new -key key.pem -out csr.pem
```

Create the self-signed certificate :
```shell
openssl x509 -req -in csr.pem -signkey key.pem -out cert.pem
```