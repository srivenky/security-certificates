# security-certificates

Step 1: Install Git<br/>
Step 2: Create a Private key <br/>
"C:\Program Files\Git\usr\bin\openssl" genrsa -out keypair.pem 2048<br/>
Step 3: Create Pub;ic Certificate from private key<br/>
"C:\Program Files\Git\usr\bin\openssl" rsa -in keypair.pem -pubout -out publickey.crt<br/>
Step 4: Create pkcs8 file<br/>
"C:\Program Files\Git\usr\bin\openssl" pkcs8 -topk8 -inform PEM -outform PEM -nocrypt -in keypair.pem -out pkcs8.key<br/>
