# Task 1

  ## Question - Read the words, and understand the meanings! Is base64 encryption or encoding?

    - Answer - 'enconding'

# Task 2

  ## Question - What is the output size in bytes of the MD5 hash function?

    ## Answer - '16'

  ## Question - Can you avoid hash collisions? (Yea/Nay)

     Answer - 'Nay'

  ## Question - If you have an 8 bit hash output, how many possible hashes are there?

     Answer - '256'
  
# Task 3

  ## Question - Crack the hash "d0199f51d2728db6011945145a1b607a" using the rainbow table manually.
    
     Answer - 'basketball'
    
  ## Question - Crack the hash "5b31f93c09ad1d065c0491b764d04933" using online tools

     Answer - 'tryhackme'
    
  ## Question - Should you encrypt passwords? Yea/Nay

     Answer - 'Nay'
    
# Task 4 

  ## Question - How many rounds does sha512crypt ($6$) use by default?

     Answer - '5000'
    
  ## Question - What's the hashcat example hash (from the website) for Citrix Netscaler hashes?

     Answer - '1765058016a22f1b4e076dccd1c3df4e8e5c0839ccded98ea'
    
  ## Question - How long is a Windows NTLM hash, in characters?

     Answer - '32'
    
# Task 5

  ## Question - Crack this hash: $2a$06$7yoU3Ng8dHTXphAg913cyO6Bjs3K5lBnwq5FJyA6d01pMSrddr1ZG

     Answer - '85208520'

Access "https://www.tunnelsup.com/hash-analyzer/" 
Insert the hash in the tool so that the identification can be done.

<img src = "https://github.com/patrickpca/TryHackMe/blob/master/Hashing%20-%20Crypto%20101/IMG/img1.PNG" width="80%">

Knowing that has is the bcrypt. Let's now use *hashcat*. Remember, never use *--force* in command, this can generate a false positive.

The function for hashcat - *hashcat -m [value] [file.txt] [path the rocktyou.txt]*

Let's find out what *value* needs to be insert into the funcion. For this we will use the command - *hashcat -h | grep -e "bcrypt*.

<img src = "https://github.com/patrickpca/TryHackMe/blob/master/Hashing%20-%20Crypto%20101/IMG/img2.PNG" width="80%">

Find out the value 3200.

Create one file *hash.txt* with the value of the question.

run the above command. It look like this *hashcat -m 3200 hash1.txt /usr/share/wordlists/rockyou.txt*

<img src = "https://github.com/patrickpca/TryHackMe/blob/master/Hashing%20-%20Crypto%20101/IMG/img3.PNG" width="80%">

  ## Question - Crack this hash: 9eb7ee7f551d2f0ac684981bd1f1e2fa4a37590199636753efe614d4db30e8e1
  
     Answer - 'halloween'
    
We can finish this question with a single site search. "https://hashes.com/en/tools/hash_identifier"

<img src = "https://github.com/patrickpca/TryHackMe/blob/master/Hashing%20-%20Crypto%20101/IMG/img4.PNG" width="80%"> 

The method of previous question is just as applicable here, just repeat the process described. - the command in Kali is *hashcat -m 1400 hash1.txt /usr/share/wordlists/rockyou.txt'*
(Remember to change the content of hash1.txt to the question hash)

  ## Question - Crack this hash: $6$GQXVvW4EuM$ehD6jWiMsfNorxy5SINsgdlxmAEl3.yif0/c3NqzGLa0P.S7KRDYjycw5bnYkF5ZtB8wQy8KnskuWQS3Yr1wQ0
     Answer - 'spaceman'

Here we will again use the site to analyze the hash and the procedure with kali can also be repeated.

  ## Question - Bored of this yet? Crack this hash: b6b0d451bbf6fed658659a9e7e5598fe
     Answer - funforyou

Here find out difficulty in executin the command in kali as rocketyou.txt does not meet the hash requirements. Finally, the site described above can easily solve it.

# Task 6
  
  ## Question - What's the SHA1 sum for the amd64 Kali 2019.4 ISO? http://old.kali.org/kali-images/kali-2019.4/
    Answer - 186c5227e24ceb60deb711f1bdc34ad9f4718ff9  

It only takes a little bit of searching on the givem site to find the hash. 
Click on the first file called "SHA1SUMS" and the first hash that appears is the flag.


  ## Question - What's the hashcat mode number for HMAC-SHA512 (key = $pass)?
    Answer - 1750

The command *hashcat -h | grep -e "HMAC-SHA512"* Will be enough to find the necessary answer. 

<img src = "https://github.com/patrickpca/TryHackMe/blob/master/Hashing%20-%20Crypto%20101/IMG/img5.PNG" width="80%">

