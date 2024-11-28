### SSH Agent Forwarding

>It is used when we are connecting a bastion box/dial box and further to a box. here to connect to private instance from dial box and hence, needed private key further to connect and so, needed to upload the key in dial box. This is having security threat if someone compromise the box then all the keys gone. so the solution for this is ssh agent forwarding. takeaway from these step

<details><summary> Add key in Key-Chain</summary>

```
ssh-add -l
ssh-add -K yourkey.pem
```
</details>
<details><summary> Validate whether it is added</summary>

```
ssh-add -l
```
</details>
<details><summary> Once added then try to connect to bastion box using the command </summary>

```
ssh -A user-name@ip-address 
```
> Here, we are not using -i and your privatekey.pem, instead -A for agent
</details>

<details><summary> Once, connected to bastion host, we will validate whether agent forwarded the key or not </summary>

```
ssh-add -l
```
> Here, we will find key in key-chain
</details>
<details><summary> Then we can connect to private box using , simple ssh command as below</summary>

```
ssh -A username@ipaddressofprivatebox 
```
</details>





