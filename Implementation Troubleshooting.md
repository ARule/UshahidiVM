# Issue Accessing Ushahidi in the VM #

  **These instructions follow Step 16 in the Ushahidi VM Installation.
  Error states: “Sorry, something went wrong. Try reloading the page.”**

1. Close the current server connection with Ctrl c in the MATE Terminal
1. Go into Applications > System Tools > MATE Terminal 
1. Change the directory to platform-client with the command `cd platform-client`
1. Use `ls -a` command to peruse directory contents
    1. `ls -a` shows hidden files and folders
1. Use `cat .env` command
    1. Allows user to find .env file
    1. Look at the first backend URL
        1. This URL must match up with IP address in the network connection settings. **Follow step 13 to find this URL**
        1. If the backend url in the terminal doesn't match the IP address, then the backend URL needs to be changed
        1. To change the backend URL, edit the .env using the command `pluma .env`. This will open up a simple text editor to change the address. Edit the first backend url to match the IP address in the network connection settings, save and close
1. Run `cat .env` to ensure that it saved correctly and matches with the IP address from the network connection settings
1. Run `ifconfig` command to verify that either two addresses below match up with the IP addresses from the network connection settings
    1. Enpos3 - inet address
       1. Should match up with the IP address under Wired Connection 1 under IPv4
    1. Enpos8 - inet address
       1. Should match up with the IP address under Wired Connection 2 under IPv4
    1. If there is a discrepency between addresses run `pluma .env` command and follow the next 3 steps
       1. This will open up a simple text editor to change the address
    1. Edit backend URL (1st one) 
       1. What URL should be: 192.168.56.101
    1. Save the edit
    1. Run `cat .env` in terminal again to ensure it is correct/saved
1. Run `npm run watch` command
    1. NOTE: Go back to the Ushahidi VM Installation instructions and keep going from Step 12
