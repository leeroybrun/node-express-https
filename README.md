# node-express-https

Example of using Express &amp; Node.js with HTTPS.

## Usage

Install dependencies :

```shell
npm install
```

Then launch the app.js file with node :

```shell
node app.js
```

You can then access the server on the address : https://127.0.0.1:8443/

## Generate the certificate

The certificate files are stored inside the `ssl/` folder. You can generate new files with the following commands.

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

Alternatively you can send the CSR to a Certificate Authority for signing.
