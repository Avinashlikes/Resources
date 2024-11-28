## SCP 
> SCP (Secure Copy Protocol) is a network protocol that securely copies files/folders between Linux (Unix) systems on a network. To transmit, use the scp command line utility, a safer variant of the cp (copy) command.

##### Use the SCP command in the following cases 
<details><summary> Copying files from a local host to a remote host. </summary>

```
scp -i key.pem Desktop/sample_example.txt root@192.168.2.1:/home/remote_dir 
```

_The command includes the following information:_

> - **Desktop/sample_example.txt** - The name of the file being copied and its location.
> - **root@192.168.2.1** - The username and IP address of the remote server.
> - **/home/remote_dir** - The location where to store the copied file.
</details>

<details><summary>Copying files from a remote host to a local host. </summary>

```
scp -i key.pem 192.168.2.1:/home/remote_dir/sample_example.txt home/Desktop
```
_The information provided is_

> - **root@192.168.2.1**- The username and IP address of the remote server from where the file is currently located.
> - **/home/remote_dir/sample_example.txt** - The name of the file being copied and its location.
> - **home/Desktop** - The location where to store the copied file.
</details>

<details><summary> Copying files between two remote servers.</summary>
  
```
scp -i key.pem root@192.168.1.2:/home/remote_dir/sample_example.txt avi@192.168.2.1:home/Desktop
```

_The command above specifies:_

> - **root@192.168.1.2** - The username and IP address of the remote server from where the file is currently located.
> - **/home/remote_dir/sample_example.txt** - The name of the file being copied and its location.
> - **Avi@192.168.2.1** - The username and IP address of the remote server where we want to copy the file.
> - **home/Desktop** - The location where to store the copied file on the remote server.
</details>
