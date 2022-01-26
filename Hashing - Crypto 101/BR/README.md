# Task 1

  ## Questão - Read the words, and understand the meanings! Is base64 encryption or encoding?

    ## Resposta - 'enconding'

# Task 2

  ## Questão - What is the output size in bytes of the MD5 hash function?

    ## Resposta - '16'

  ## Questão - Can you avoid hash collisions? (Yea/Nay)

    ## Reposta - 'Nay'

  ## Questão - If you have an 8 bit hash output, how many possible hashes are there?

    ## Repostas - '256'
  
# Task 3

  ## Questão - Crack the hash "d0199f51d2728db6011945145a1b607a" using the rainbow table manually.
    
    ## Resposta - 'basketball'
    
  ## Crack the hash "5b31f93c09ad1d065c0491b764d04933" using online tools

    ## Resposta - 'tryhackme'
    
  ## Should you encrypt passwords? Yea/Nay

    ## Resposta - 'Nay'
    
# Task 4 

  ## Questão - How many rounds does sha512crypt ($6$) use by default?

    ## Resposta - '5000'
    
  ## Questão - What's the hashcat example hash (from the website) for Citrix Netscaler hashes?

    ## Resposta - '1765058016a22f1b4e076dccd1c3df4e8e5c0839ccded98ea'
    
  ## Questão - How long is a Windows NTLM hash, in characters?

    ## Resposta - '32'
    
# Task 5

  ## Questão - Crack this hash: $2a$06$7yoU3Ng8dHTXphAg913cyO6Bjs3K5lBnwq5FJyA6d01pMSrddr1ZG

    ## Resposta - '85208520'

Necessário acessar "https://www.tunnelsup.com/hash-analyzer/" 
Insira o hash na ferramenta para que possa ser feito a identificação do Hash utilizado.
<img src = "https://github.com/patrickpca/TryHackMe/blob/master/Hashing%20-%20Crypto%20101/IMG/img1.PNG" width="40%">

Conhecendo que bcrypt é o hash utilizado. Vamos agora usar a ferramenta hashcat, lembrando que não se deve usar --force no comando, isso pode gerar um falso positivo.

A função para o hashcat - 'hashcat -m [valor] [arquivo.txt] [caminho do rocktyou.txt]'

Vamos descobrir qual o valor que é necessário ser inserido na função. Para isso usaremos o comando - 'hashcat -h | grep -e "bcrypt"', assim podes saber o valor para o hash que desejamos.

<img src = "https://github.com/patrickpca/TryHackMe/blob/master/Hashing%20-%20Crypto%20101/IMG/img2.PNG" width="40%">

Encontrado o valor de 3200.

Criar um arquivo hash.txt com o valor da hash da questão.

execute o comando acima. Vai ficar parecido com isso - 'hashcat -m 3200 hash1.txt /usr/share/wordlists/rockyou.txt'

<img src = "https://github.com/patrickpca/TryHackMe/blob/master/Hashing%20-%20Crypto%20101/IMG/img3.PNG" width="40%">

  ## Questão - Crack this hash: 9eb7ee7f551d2f0ac684981bd1f1e2fa4a37590199636753efe614d4db30e8e1
  
    ## Resposta - 'halloween'
    
Podemos finalizar essa questão com uma única pesquisa no site "https://hashes.com/en/tools/hash_identifier". Basta apenas inserir a hash na coluna e prontinho.

<img src = "https://github.com/patrickpca/TryHackMe/blob/master/Hashing%20-%20Crypto%20101/IMG/img4.PNG" width="40%"> 

O método da questão anterior tão se aplica aqui, so repetir o processo descrito. - o comando no Kali fica 'hashcat -m 1400 hash1.txt /usr/share/wordlists/rockyou.txt'
(Lembre de mudar o conteúdo do hash1.txt para o hash da questão)

  ## Questão - Crack this hash: $6$GQXVvW4EuM$ehD6jWiMsfNorxy5SINsgdlxmAEl3.yif0/c3NqzGLa0P.S7KRDYjycw5bnYkF5ZtB8wQy8KnskuWQS3Yr1wQ0
    ## Resposta - 'spaceman'

Aqui usaremos novamente o site para analisar o hash e o procedimento com o kali também pode ser repetido.

  ## Questão - Bored of this yet? Crack this hash: b6b0d451bbf6fed658659a9e7e5598fe
    ## Resposta - funforyou

Aqui teremos dificuldade em executar o comando no Kali já que o rocktyou.txt não atende os requisitos da hash. Por fim, o site descrito anteriormente consegue facilmente resolver.
