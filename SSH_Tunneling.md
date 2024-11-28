#### SSH Tunneling
> SSH tunneling, also known as SSH port forwarding, is a method of sending data over an encrypted connection using the Secure Shell (SSH) protocol. It allows users to forward connections made to a local port on their device to a remote machine through a secure channel. SSH tunneling enables users to access resources or services on a remote server that may be inaccessible due to network limitations or firewall settings. For example, a user can use SSH tunneling to redirect a local port to the remote server's port if direct access to the remote server's port is blocked.

<details><summary>Step 1: SSH Command to connect server</summary>

  > Step 1: SSH Command to connect server
```
ssh -i ./.ssh/sj03 user@domain.com
```

</details>
<details><summary>Step 2: Add -N to Network Port Forward</summary>

  > Step 2: Add -N to Network Port Forward
```
 ssh -i ./.ssh/sj03 user@domain.com -N
```
</details>
<details><summary>Step 3: Add -L if tunnel starts on Local</summary>

  > Step 3: Add -L if tunnel starts on Local Port 8888
```
SSH -i ./.ssh/sj03 user@domain.com -N -L 8888
```
</details>
<details><summary>Step 4: Add -R if tunnel starts on Remote</summary>

 > Step 4: Add -R if tunnel starts on Remote PORT 80
```
 ssh -i ./.ssh/sj03 user@domain.com -N -R 80
```
</details>
<details><summary>Step 5: Open Local Port 8510 and forward to <remote-server> on Port 22</summary>

  > Step 5: Open Local Port 8510 and forward to <remote-server> on Port 22
```
ssh -i ./.ssh/sj03 user@domain.com -N -L 8510:<remote-server-ip-you-want-to-connect>:22
```
</details>
<details><summary> Step 6: Now Local Port is open , connect your server </summary>

  > Step 6: Now Local Port is open , connect your server
```
ssh -i ./.ssh/sj03 user@localhost -p 8510
``` 
</details>



