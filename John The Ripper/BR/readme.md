# Task 1
  ### `Sem Questão`
  
# Task 2
  ## Questão - What is the most popular extended version of John the Ripper?
  ### Reposta - `Jumbo John`
  
# Task 3
  ## Questão - What is the most popular extended version of John the Ripper?
  ### Resposta -  `rockyou.com`

# Task 4 
  ## Questão - What type of hash is hash1.txt?
  ### Resposta - `md5`

  ## Questão - What is the cracked value of hash1.txt?
  ### Resposta - `biscuit`

Acesse sua maquina Kali e baixe o arquivo *First_task_hashes*.
Abra o arquivo hash1.txt - copie a hash e insira no site recomendado - https://hashes.com/en/tools/hash_identifier

<img src = "img1.png" width="80%">

TryHackme sugere o uso da ferramenta john. Então vamos usa-la.
Usando a o *hash-identifier* identificamos o tipo de hash usado.

<img src = "img2.png" width="80%">

identificado o hash, vamos para o *JOHN*.

O comando para executar o é john --format=[tipo hash] --wordlist=[caminho do wordlist] [caminho hash1.txt].

<img src = "img3.png" width="80%">

   ## Questão - What type of hash is hash2.txt?
   ### Resposta - `SHA1`
   
   ## Questão - What is the cracked value of hash2.txt
   ### Resposta - `kangeroo`

O mesmo passo-a-passo é realizado.

<img src = "img4.png" width="80%">

<img src = "img5.png" width="80%">

   ## Questão - What type of hash is hash3.txt?
   ### Resposta - `SHA256`
   
   ## Questão - What is the cracked value of hash3.txt
   ### Resposta - `microphone`
   
   ## Questão - What type of hash is hash4.txt?
   ### Resposta - `whirlpool`
   
   ## Questão - What is the cracked value of hash4.txt
   ### Resposta - `colossal`
   
# Task 5
   ## Questão - What do we need to set the "format" flag to, in order to crack this?
   ### Resposta - `NT`
   
   ## What is the cracked value of this password?
   ### Resposta - `mushroom`

<img src="img6.png" width="80%">

<img src="img7.png" width="80%">

# Task 6
   ## Questão - What is the root password?
   ### Resposta - `1234`

Com o arquivo *etchashes.txt* no pc, podemos executar alguns comandos que permitiram encotrar a solução.

o commando *unshadow [caminho do passwd] [caminho do shadow]* é o que vai gerar um arquivo txt para ser executado pelo john.

<img src = "img8.png" width="80%">

<img src = "img9.png" width="80%">

