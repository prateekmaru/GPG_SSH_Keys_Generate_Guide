---
title: GPG Key && SSH Key Generate Guide  For Git
updated: 2022-08-12 17:22:05Z
created: 2022-08-12 17:01:39Z
---
# GPG Key && SSH Key Generate Guide  For Git
# For GPG Key

  prateek@Arc13x~/Desktop 
❯ gpg --version
gpg (GnuPG) 2.3.7
libgcrypt 1.10.1-unknown
Copyright (C) 2021 Free Software Foundation, Inc.
License GNU GPL-3.0-or-later &lt;https://gnu.org/licenses/gpl.html&gt;
This is free software: you are free to change and redistribute it.
There is NO WARRANTY, to the extent permitted by law.

Home: /home/prateek/.gnupg
Supported algorithms:
Pubkey: RSA, ELG, DSA, ECDH, ECDSA, EDDSA
Cipher: IDEA, 3DES, CAST5, BLOWFISH, AES, AES192, AES256, TWOFISH,
        CAMELLIA128, CAMELLIA192, CAMELLIA256
AEAD: EAX, OCB
Hash: SHA1, RIPEMD160, SHA256, SHA384, SHA512, SHA224
Compression: Uncompressed, ZIP, ZLIB, BZIP2
  prateek@Arc13x~/Desktop 
❯ gpg --full-generate-key
gpg (GnuPG) 2.3.7; Copyright (C) 2021 Free Software Foundation, Inc.
This is free software: you are free to change and redistribute it.
There is NO WARRANTY, to the extent permitted by law.

Please select what kind of key you want:
   (1) RSA and RSA
   (2) DSA and Elgamal
   (3) DSA (sign only)
   (4) RSA (sign only)
   (9) ECC (sign and encrypt) \*default\*
  (10) ECC (sign only)
  (14) Existing key from card
Your selection? 1
RSA keys may be between 1024 and 4096 bits long.
What keysize do you want? (3072) 4096
Requested keysize is 4096 bits
Please specify how long the key should be valid.
         0 = key does not expire
      &lt;n&gt;  = key expires in n days
      &lt;n&gt;w = key expires in n weeks
      &lt;n&gt;m = key expires in n months
      &lt;n&gt;y = key expires in n years
Key is valid for? (0) 0
Key does not expire at all
Is this correct? (y/N) Y

GnuPG needs to construct a user ID to identify your key.

Real name: Prateek Maru
Email address: prateekmaru@yahoo.com
Comment: 
You selected this USER-ID:
    "Prateek Maru &lt;prateekmaru@yahoo.com&gt;"

Change (N)ame, (C)omment, (E)mail or (O)kay/(Q)uit? O
We need to generate a lot of random bytes. It is a good idea to perform
some other action (type on the keyboard, move the mouse, utilize the
disks) during the prime generation; this gives the random number
generator a better chance to gain enough entropy.
We need to generate a lot of random bytes. It is a good idea to perform
some other action (type on the keyboard, move the mouse, utilize the
disks) during the prime generation; this gives the random number
generator a better chance to gain enough entropy.
gpg: directory '/home/prateek/.gnupg/openpgp-revocs.d' created
gpg: revocation certificate stored as '/home/prateek/.gnupg/openpgp-revocs.d/BBB6F6FD71C51044EAE9B8152A0C86CF17FFB466.rev'
public and secret key created and signed.

pub   rsa4096 2022-08-12 \[SC\]
      BBB6F6FD71C51044EAE9B8152A0C86CF17FFB466
uid                      Prateek Maru &lt;prateekmaru@yahoo.com&gt;
sub   rsa4096 2022-08-12 \[E\]

 1m 34.158s  prateek@Arc13x ~/Desktop 
❯ gpg --armor --export BBB6F6FD71C51044EAE9B8152A0C86CF17FFB466
-----BEGIN PGP PUBLIC KEY BLOCK-----

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
51kY
=uojs
-----END PGP PUBLIC KEY BLOCK-----
  prateek@Arc13x~/Desktop 
❯ git config --global user.signingkey 2A0C86CF17FFB466
  prateek@Arc13x~/Desktop 
❯ git config --global commit.gpgsign true
  prateek@Arc13x~/Desktop 
❯ git config --global gpg.program gpg
  prateek@Arc13x~/Desktop 
❯ export GPG_TTY=$(tty)
  prateek@Arc13x~/Desktop 
❯ 

* * *

# For SSH Key

  prateek@Arc13x~/Desktop 
❯ ls -al ~/.ssh 
ls: cannot access '/home/prateek/.ssh': No such file or directory
 2  prateek@Arc13x ~/Desktop 
❯ ssh-keygen -t rsa -b 4096 -C "prateekmaru@yahoo.com"  
Generating public/private rsa key pair.
Enter file in which to save the key (/home/prateek/.ssh/id_rsa): 
Created directory '/home/prateek/.ssh'.
Enter passphrase (empty for no passphrase): 
Enter same passphrase again: 
Your identification has been saved in /home/prateek/.ssh/id_rsa
Your public key has been saved in /home/prateek/.ssh/id_rsa.pub
The key fingerprint is:
SHA256:UhvrJjH2lWgzpawcDxDxFFpPeZzvGahQd48kik89NRI prateekmaru@yahoo.com
The key's randomart image is:
+---\[RSA 4096\]----+
|    o.+..oEo     |
|     \* oo B =    |
|    o .o+=.O +   |
|     .oooB+.+ .  |
|      B+S.oo o   |
|     o %o+  o    |
|      \+ =        |
|       o         |
|                 |
+----\[SHA256\]-----+
 1m 2.237s  prateek@Arc13x ~/Desktop 
❯  ls -al ~/.ssh        
total 12K
drwx------. 1 prateek prateek   32 Aug 12 22:24 **.**
drwx------. 1 prateek prateek  784 Aug 12 22:23 **..**
-rw-------. 1 prateek prateek 3.4K Aug 12 22:24 id_rsa
-rw-r--r--. 1 prateek prateek  747 Aug 12 22:24 id_rsa.pub
  prateek@Arc13x~/Desktop 
❯ eval "$(ssh-agent -s)"
Agent pid 19328
  prateek@Arc13x~/Desktop 
❯ ssh-add ~/.ssh/id_rsa 
Enter passphrase for /home/prateek/.ssh/id_rsa: 
Identity added: /home/prateek/.ssh/id_rsa (prateekmaru@yahoo.com)
 9.533s  prateek@Arc13x ~/Desktop 
❯ clip < ~/.ssh/id_rsa.pub

* * *

> ### For Workspace GPG Key Must Required for each commit verification
> 
> Passphrase Must be unique
> Add GPG Key && SSH Key Public Key After Login into Github && GitLab
> 
> `This Best Practices for  git users`
> 
> Each Keys Are Unique // You cant copy my key xD

![c77e2697d60f1016ef97c2f090502d7b.png](/_resources/c77e2697d60f1016ef97c2f090502d7b.png)