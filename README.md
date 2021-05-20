# security-certificates

Step 1: Install Git
Step 2: Create a Private key 
"C:\Program Files\Git\usr\bin\openssl" genrsa -out keypair.pem 2048
Step 3: Create Pub;ic Certificate from private key
"C:\Program Files\Git\usr\bin\openssl" rsa -in keypair.pem -pubout -out publickey.crt
Step 4: Create pkcs8 file
"C:\Program Files\Git\usr\bin\openssl" pkcs8 -topk8 -inform PEM -outform PEM -nocrypt -in keypair.pem -out pkcs8.key
