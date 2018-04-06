Run: "sudo apt install chrony"

Copy the configuration file into /etc/chrony/, replacing what is already there. This config file contains the IP address of the server that the time is gotten from.

Run: "invoke-rc.d chrony restart"
