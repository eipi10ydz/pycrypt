## pycrypt
### main idea
- Encryption
   - divide a file to fragments
   - generate 16 random bytes for 128 bits AES key
   - use RSA public key to encrypt AES key
   - use AES key to encrypt files
- Decryption
   - divide an encrypted file to fragments
   - use RSA private key to decrypt AES key
   - use AES key to decrypt files
   - merge the fragments

### usage
```bash
sudo pip install -r requirements.txt 
./pycrypt -h
```

### examples
```bash
./pycrypt -e file_to_be_encrypted -k id_rsa.pub [-o encrypted_file]
./pycrypt -d file_to_be_decrypted -k id_rsa [-o decrypted_file]
```