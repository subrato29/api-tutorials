- HTTP
	- data transfer(request/response) done in plain text via public network
	- default port no: 80
	- insecured
	- light weight
	- OSI layer 7- Application layer

- HTTPS
	- secured
	- data transfer will be done in encrypted form
	- default port no: 443
	- Certificate authority(CA)- applicable at browser side
	- Heavier that HTTP

	- 2 types of security involves
		- SSL: Secured socket layer(old one, less secured than TLS)
		- TLS: Transport layer security(advance version of SSL, more secured that SSL)

	- 2 types of SSL/TLS encryption
		- Assymmetric 
			- More and highly secured to crack
			- Public key(with the client sent by server to encrypt the data)
			- Private key(with the server to decrypt the data)
			- heavier than Symmetric encryption. It take 1024 to 2048 bits.
		- Symmetric
			- Common key send out from Server to client.
			- Common key is responsible for encryption/decryption of data.
			
	- For highly secrured model: Assymmetric + Symmetric
		- public key(assymmetric) + CA is sent out by server to the client(browser) => Assymmetric protocol
		- client(browser) will generate a symmetric(local) session key => Symmetric protocol
		- (Assymmetric public key + Symmetric session key) will be sent to the server
		- Server will be having one asymmetric private key
		- Server will decrypt the session key using asymmetric private key
		- Now the connection(session) will be established between client and server

