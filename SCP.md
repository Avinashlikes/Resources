#### SCP (Secure Copy Protocol) is a network protocol that securely copies files/folders between Linux (Unix) systems on a network. To transmit, use the scp command line utility, a safer variant of the cp (copy) command.


<details><summary> Use the SCP command in the following cases </summary>

> Copying files from a local host to a remote host.

```
scp -i key.pem Desktop/sample_example.txt root@192.168.2.1:/home/remote_dir 
```

The command includes the following information:

- **Desktop/sample_example.txt** - The name of the file being copied and its location.
- **root@192.168.2.1** - The username and IP address of the remote server.
- **/home/remote_dir** - The location where to store the copied file.

> Copying files from a remote host to a local host.

```
scp -i key.pem 192.168.2.1:/home/remote_dir/sample_example.txt home/Desktop
```
The information provided is

- **root@192.168.2.1**- The username and IP address of the remote server from where the file is currently located.
- **/home/remote_dir/sample_example.txt** - The name of the file being copied and its location.
- **home/Desktop** - The location where to store the copied file.

> Copying files between two remote servers.

```
scp -i key.pem root@192.168.1.2:/home/remote_dir/sample_example.txt avi@192.168.2.1:home/Desktop
```

The command above specifies:

- **root@192.168.1.2** - The username and IP address of the remote server from where the file is currently located.
- **/home/remote_dir/sample_example.txt** - The name of the file being copied and its location.
- **Avi@192.168.2.1** - The username and IP address of the remote server where we want to copy the file.
- **home/Desktop** - The location where to store the copied file on the remote server.
</details>
