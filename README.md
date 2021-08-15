# Incubator

To run patched version of code you need to: 

  - Install the following python modules
  ```
  pip3 install python-dotenv  
  pip3 install scapy
  pip3 install python3-dtls
  ```
  - create a .env in same directory as the Client and Server. Add a password to .env as shown below  
  ```
  AUTH='!Q#E%T&U8i6y4r2w'  
  ```  
  - create ssl certificate and private key (in our example we left everything blank for the CSR, including password)
  ```
  openssl genrsa -out privkey.pem 2048
  openssl req -new -key privkey.pem -out signreq.csr
  openssl x509 -req -days 365 -in signreq.csr -signkey privkey.pem -out certificate.pem
  ```
