# Issue accessing Ushahidi in the VM #

  These instructions follow Step 16 in the Ushahidi VM Installation
  Error states: “Sorry, something went wrong. Try reloading the page.”
  
1. Go into Applications > System Tools > MATE Terminal
2. If not already, change directory ‘cd’ into platform-client
3. Look at the contents of this directory using the command ‘ls -a’. 
    3. This command is different than ‘ls’ because it shows hidden files and folders


Look in the .env file using the command ‘cat .env’
Look at the backend URL. This URL must match up with IP address in the network connection settings. Follow step 13 to find this URL
If the backend url doesn't match the IP address, then the backend needs to be edited
To edit the .env use the command ‘pluma .env’. This will open up a simple text editor to change the address. Edit the first backend url to match and save


Run ‘cat .env’ to ensure that it saved
Run the command ‘ifconfig’
Look at enpos8’s inet address 
It should match with the IP address in the network connection settings within the VM (dual arrows)- This is the area that you looked at in step 13b.
If not, the .env file will need to be edited. Use ‘pluma .env’ to edit the first backend URL. 
Example:It should say 192.168.56.101
Save & Edit the .env file
Run ‘cat .env’ again to ensure it was saved once more
Now use ‘npm run watch’ command
NOTE: ‘Npm run watch’ command runs scripts from package.json when files change
Pick back up with Step 12 and run through the rest of the instructions found on GitHub


