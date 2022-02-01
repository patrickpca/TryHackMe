
##### Task 2

###### Questão - Are SSH keys protected with a passphrase or a password?
###### Resposta - `passphrase`   -> Separada da chave, é semelhante a uma senha que é usada para proteger uma chave.

##### Task 3

###### Questão - What does SSH stand for?
###### Resposta - `secure shell`   

###### Questão - How do webservers prove their identity?
###### Resposta - `certificate`   

###### Questão - What is the main set of standards you need to comply with if you store or process payment card details?
###### Resposta - `PCI-DSS`   

#### Task 4

##### Questão - What's 30 % 5?
##### Resposta - `0`

##### Questão - What's 25 % 7
##### Resposta - `4`

##### Questão - What's 118613842 % 9091
##### Resposta - `3565` -> Utlize o *Colab* para realizar a conta.

#### Task 5

##### Questão - Should you trust DES? Yea/Nay
##### Resposta - `Nay`

##### Questão - What was the result of the attempt to make DES more secure so that it could be used for longer?
##### Resposta - `Triple DES`

##### Questão - Is it ok to share your public key? Yea/Nay?
##### Resposta - `Yea`

#### Task 6

##### Questão - p = 4391, q = 6659. What is n?
##### Resposta - `29239669`

#### Task 8

##### Questão - Who is TryHackMe's HTTPS certificate issued by?
##### Resposta - `r3`

<img src="https://github.com/patrickpca/TryHackMe/blob/master/Encryption%20-%20Crypto%20101/img/img1.PNG" width="50%">

Em seguida -> Clique em conexão segura -> Clique em O certifciado é valido.

<img src="https://github.com/patrickpca/TryHackMe/blob/master/Encryption%20-%20Crypto%20101/img/img2.PNG" width="50%">

#### Task 9

##### Questão - What algorithm does the key use?
##### Resposta - `rsa`

##### Questão - Crack the password with John The Ripper and rockyou, what's the passphrase for the key?
##### Resposta - `delicious`

Baixa o arquivo idrsa.id_rsa -> use a ferramente *ssh2john* para fazer da chave um hash -> use *john* para identificar a mesagem encodada.

<img src ="https://github.com/patrickpca/TryHackMe/blob/master/Encryption%20-%20Crypto%20101/img/img3.PNG" width="70%">

<img src ="https://github.com/patrickpca/TryHackMe/blob/master/Encryption%20-%20Crypto%20101/img/img4.PNG" width="70%">


#### Task 11

##### Questão - You have the private key, and a file encrypted with the public key. Decrypt the file. What's the secret word?
##### Resposta - `Pineapple`

Baixe o arquivo gpg.zip -> descompacte `unzip gpg.zip` 

Importar a chave para o comando gpg -> `gpg --import tryhackme.key`

Executar o gpg -> `gpg message.gpg`

Visualize o conteudo no novo arquivo -> `cat message`

<img src ="https://github.com/patrickpca/TryHackMe/blob/master/Encryption%20-%20Crypto%20101/img/img5.PNG" width="70%">

<img src ="https://github.com/patrickpca/TryHackMe/blob/master/Encryption%20-%20Crypto%20101/img/img6.PNG" width="70%">

<img src ="https://github.com/patrickpca/TryHackMe/blob/master/Encryption%20-%20Crypto%20101/img/img7.PNG" width="20%">








