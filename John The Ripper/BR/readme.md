#### - Task 1
  ##### `Sem Questão`
  
#### - Task 2
  ##### Questão - What is the most popular extended version of John the Ripper?
  ##### Reposta - `Jumbo John`
  
#### - Task 3
  ##### Questão - What is the most popular extended version of John the Ripper?
  ##### Resposta -  `rockyou.com`

#### - Task 4 
  ##### Questão - What type of hash is hash1.txt?
  ##### Resposta - `md5`

  ##### Questão - What is the cracked value of hash1.txt?
  ##### Resposta - `biscuit`

Acesse sua maquina Kali e baixe o arquivo *First_task_hashes*.
Abra o arquivo hash1.txt - copie a hash e insira no site recomendado - https://hashes.com/en/tools/hash_identifier

<img src = "https://github.com/patrickpca/TryHackMe/blob/master/John%20The%20Ripper/img/img1.PNG" width="80%">

TryHackme sugere o uso da ferramenta john. Então vamos usa-la.
Usando a o *hash-identifier* identificamos o tipo de hash usado.

<img src = "https://github.com/patrickpca/TryHackMe/blob/master/John%20The%20Ripper/img/img2.PNG" width="80%">

identificado o hash, vamos para o *JOHN*.

O comando para executar o é john --format=[tipo hash] --wordlist=[caminho do wordlist] [caminho hash1.txt].

<img src = "https://github.com/patrickpca/TryHackMe/blob/master/John%20The%20Ripper/img/img3.PNG" width="80%">

   ##### Questão - What type of hash is hash2.txt?
   ##### Resposta - `SHA1`
   
   ##### Questão - What is the cracked value of hash2.txt
   ##### Resposta - `kangeroo`

O mesmo passo-a-passo é realizado.

<img src = "https://github.com/patrickpca/TryHackMe/blob/master/John%20The%20Ripper/img/img4.PNG" width="80%">

<img src = "https://github.com/patrickpca/TryHackMe/blob/master/John%20The%20Ripper/img/img5.PNG" width="80%">

   ##### Questão - What type of hash is hash3.txt?
   ##### Resposta - `SHA256`
   
   ##### Questão - What is the cracked value of hash3.txt
   ##### Resposta - `microphone`
   
   ##### Questão - What type of hash is hash4.txt?
   ##### Resposta - `whirlpool`
   
   ##### Questão - What is the cracked value of hash4.txt
   ##### Resposta - `colossal`
   
#### - Task 5
   ##### Questão - What do we need to set the "format" flag to, in order to crack this?
   ##### Resposta - `NT`
   
   ##### What is the cracked value of this password?
   ##### Resposta - `mushroom`

<img src="https://github.com/patrickpca/TryHackMe/blob/master/John%20The%20Ripper/img/img6.PNG" width="80%">

<img src="https://github.com/patrickpca/TryHackMe/blob/master/John%20The%20Ripper/img/img7.PNG" width="80%">

#### - Task 6
   ##### Questão - What is the root password?
   ##### Resposta - `1234`

Com o arquivo *etchashes.txt* no pc, podemos executar alguns comandos que permitiram encotrar a solução.

o commando *unshadow [caminho do passwd] [caminho do shadow]* é o que vai gerar um arquivo txt para ser executado pelo john.

<img src = "https://github.com/patrickpca/TryHackMe/blob/master/John%20The%20Ripper/img/img8.PNG" width="80%">

<img src = "https://github.com/patrickpca/TryHackMe/blob/master/John%20The%20Ripper/img/img9.PNG" width="80%">

#### - task 7
  ##### Questão - What is Joker's password?
  ##### Resposta - `jok3r`
  
  O procedimento utilizado anteriormente é capaz de realizar a quebra do hash normalmente.
  Usando a função - *single* do john também é possível.
  
  Use o *hash-identifier* para identificar o tipo de hash usado.
  
  <img src = "https://github.com/patrickpca/TryHackMe/blob/master/John%20The%20Ripper/img/img10.PNG" width="80%">  
  
  Realizar a organização dos GECOS - Abra o arquivo *hash7.txt* é insira o usuário informado e "*:*" -> *Joker:7bf6d9bb82bed1302f331fc6b816aada*
  
  Execute o comando [*john --single --format=raw-md5 hash7.txt*]
  
  <img src = "https://github.com/patrickpca/TryHackMe/blob/master/John%20The%20Ripper/img/img11.PNG" width="80%">
  
#### - Task 8
  ##### Questão - What do custom rules allow us to exploit?
  ##### Resposta - `password complexity predictability`
  
  ##### Questão - What rule would we use to add all capital letters to the end of the word?
  ##### Resposta - `Az"[A-z]"`
  
  ##### Questão - What flag would we use to call a custom rule called "THMRules"
  ##### Resposta - `-rule=THMRules`
  
  
#### - Task 9
  ##### Questão - What is the password for the secure.zip file?
  ##### Resposta - `pass123`
  
Execute o comando *zip2john secure.zip > secure_hash.txt* para que o arquivo.zip seja convertido em hash e possa ser entendido pelo *john*. 

<img src="https://github.com/patrickpca/TryHackMe/blob/master/John%20The%20Ripper/img/img12.PNG" width="80%">

com o hash pronto, novamente é necessário o uso do comando já usado anteriormente.

<img src="https://github.com/patrickpca/TryHackMe/blob/master/John%20The%20Ripper/img/img13.PNG" width="80%">
  
  ##### Questão - "What is the contents of the flag inside the zip file?"
  ##### Resposta - `THM{w3ll_d0n3_h4sh_r0y4l}`

<img src="https://github.com/patrickpca/TryHackMe/blob/master/John%20The%20Ripper/img/img14.PNG" width="80%">
    
#### - Task 10 

  ##### Questão - What is the password for the secure.rar file?
  ##### Resposta - `password`

Executado o comando *rar2john secure.rar > secure_hash.txt* ->  para que o arquivo.rar seja convertido em hash e possa ser entendido pelo *john*. 

<img src = "https://github.com/patrickpca/TryHackMe/blob/master/John%20The%20Ripper/img/img15.PNG" width="80%">

com o hash pronto, novamente é necessário o uso do comando já usado anteriormente.

<img src = "https://github.com/patrickpca/TryHackMe/blob/master/John%20The%20Ripper/img/img16.PNG" width="80%">

  ##### Questão - What is the contents of the flag inside the zip file?
  ##### Resposta - `THM{r4r_4rch1ve5_th15_t1m3}`

Use o comando *unrar x secure.rar* e a senha encontrada. flag.txt será exportado para o diretório atual
  
  
#### - Task 11  
  ##### Questão - What is the SSH private key password?
  ##### Resposta - `mango`
  
A função *ssh2john* não estava presente no SO. 

A função *python /usr/share/ssh2john.py idrsa.id_rsa > id_hash.txt* é usado.

<img src = "https://github.com/patrickpca/TryHackMe/blob/master/John%20The%20Ripper/img/img17.PNG" width="80%">

Executar a função *john --wordlist=/usr/share/wordlist/rocketyou.txt id_hash.txt*

<img src = "https://github.com/patrickpca/TryHackMe/blob/master/John%20The%20Ripper/img/img18.PNG" width="80%">


#### - Task 12  
  ##### Questão - Read the above.
  ##### Resposta - `no answer need`
