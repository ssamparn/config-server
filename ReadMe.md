## Set up ssh in git hub for spring cloud config server to communicate with config (git) repository
```bash
$ ssh-keygen -m PEM -t rsa -b 4096 -C "sashank1703@gmail.com"
```
> Generating public/private rsa key pair.
> Enter file in which to save the key (/Users/sashankasamantray/.ssh/id_rsa):

```bash
github-rsa
```
> Enter passphrase (empty for no passphrase)
```bash
passphrase
```
```
Your identification has been saved in github-ssh
Your public key has been saved in github-ssh.pub
The key fingerprint is:
SHA256:Nle+Sx70mkyfBl2wjhKqIqzI8xQcJKcquz1KOkOyExM sashank1703@gmail.com
The key's randomart image is:
+---[RSA 4096]----+
| . o             |
|  =           .  |
| . .        .  o |
|E . .     .o  . .|
|o. o    S...o+ . |
|=o  .  ..o..ooo  |
|+* .   .   .=..  |
|X+= . .    = *.. |
|*B++ .      *.o  |
+----[SHA256]-----+
```
> RSA is not supported anymore. Use ecdsa instead.

Get the hostKey:
```bash
$ ssh-keyscan -t ecdsa github.com
```
```bash
$ ssh-keygen -t ecdsa -b 256 -C "sashank1703@gmail.com"
```
> Generating public/private ecdsa key pair.
> Enter file in which to save the key (/Users/sashankasamantray/.ssh/id_ecdsa): github-ssh-ecdsa
```bash
github-ssh-ecdsa
```
> Enter passphrase (empty for no passphrase):
```bash
passphrase
```
```
Your identification has been saved in github-ssh-ecdsa
Your public key has been saved in github-ssh-ecdsa.pub
The key fingerprint is:
SHA256:C2TtfOF5ag2rxsgsC8+Hedcc1VON5idwWmDUOzc7rR8 sashank1703@gmail.com
The key's randomart image is:
+---[ECDSA 521]---+
|           .+o ..|
|       .   .. * o|
|      o . .  O o |
|     o o . oo B.o|
|      . S =..  *+|
|       . o.*   o.|
|  .  = o.o+..  E.|
|   ++ * +oo   . .|
|    += o.      ..|
+----[SHA256]-----+
```
####References:
- https://www.youtube.com/watch?v=Zbijm8wJTTE
- https://boottechnologies-ci.medium.com/spring-cloud-config-and-git-ssh-configuration-70ab570bcf4f
- https://stackoverflow.com/questions/71378525/spring-cloud-config-throws-invalid-private-key-error
- https://stackoverflow.com/questions/71489256/spring-cloud-config-server-github-sha-1-error
- 


