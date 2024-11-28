> ### SSH (Secure Shell or Secure Socket Shell) is a network protocol that gives users -- particularly systems administrators -- a secure way to access a computer over an unsecured network. SSH also refers to the suite of utilities that implement the SSH protocol. Secure Shell provides strong password authentication and public key authentication, as well as encrypted data communications between two computers connecting over an open network, such as the internet. SSH is important for maintaining the security of systems, as the protocol acts as a secure way to provide access and management of networked systems.

#### SSH Commands

<details><summary>From Linux/Mac/Ubuntu</summary>
  
> - Connect a machine (Id = 192.168.1.2 & User Id = User)
> - Download your Key.pem & Change the mode by running this command at the file location 

```
chmod 400 Key.pem
```
> Write this command to connect your Linux machine from your local

```
ssh -i Key.pem User@192.168.1.2
```
</details>

<details><summary>Windows</summary>
<p>

</p>
</details>
