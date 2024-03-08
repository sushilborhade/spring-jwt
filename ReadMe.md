Follow below steps to generate private.pem and public.pem keys.

Before creating these keys first create temp keypair.pem. 

    openssl genrsa -out keypair.pem 2048

**Generate public key**

    openssl rsa -in keypair.pem -pubout -out public.pem

**Generate private key**

    openssl pkcs8 -topk8 -inform PEM -outform PEM -nocrypt -in keypair.pem -out private.pem

**Delete keypair.pem**
