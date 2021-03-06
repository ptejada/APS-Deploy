APS-Deploy
==========

A project that bundles together an APE Server with the ApePubSub framework.

### How to use this repository?

First of all clone the the repository ofcourse:
```
git clone https://github.com/ptejada/APS-Deploy.git
```

The previous command will clone the repository in a `APS-Deploy` directory. Change directory
```
cd APS-Deploy
```

All bundled commands will be initiated from the root. Run the `update` command:
```
./update
```
or
```
sh update
```
The first time you execute the `update` command you will be prompted to enter a port number. This port number will be the port the server will be bound to when running. You will also be prompted to name the server instance, is basically the name that will show up in the OS process listing when the server is running.

Once the `update` command finishes you may start the server:
```
./start
```

Done! Your APE_Server + ApePubSub setup is up and running! It is recommended that you setup your subdomain wildcard for user sessions comparability, refer to [Using Sessions] (https://github.com/ptejada/ApePubSub/wiki/APE-Server-setup#using-session)

### Updating

Since all files and folders that might required manual updating are carefully configured to be ignored by git, updating your clone should be pretty smooth. A simple pull will do:

```
git pull
```

All customs scripts will live in the `APScript/` folder, just make sure not to add anything on the `APScript/framework/` folder as it gets overwritten on every `update` command. 

To update all dependencies, APE_Server and ApePubSub, just run the `update` command:

```
./update
```

### Commands
<table>
	<tr>
		<th>Command</th>
		<th>Action</th>
	</tr>
	<tr>
		<td>start</td>
		<td>Starts the server if is not running</td>		
	</tr>
	<tr>
		<td>stop</td>
		<td>Kill/Terminates the server if it is running</td>		
	</tr>
	<tr>
		<td>restart</td>
		<td>Restart the server</td>		
	</tr>
	<tr>
		<td>update</td>
		<td>Fetches updates for both APE_server and ApePubSub and updates core files. Then server binaries will be re-built</td>		
	</tr>
	<tr>
		<td>debug</td>
		<td>Start the server in the foreground for ease debugging. Any errors from your scripts should be printed in the console. To exit the server use `Ctrl + c` in your keyboard</td>		
	</tr>
	<tr>
		<td>config</td>
		<td>Allows you to re-configure the server by setting the port number and instance name</td>		
	</tr>
	
</table>

### References

- [ApePubSub API](https://github.com/ptejada/ApePubSub/wiki/API)
- [APE Server API](http://www.ape-project.org/static/jsdocs/server/symbols/Ape.html)
