## Task
`Industries` system admin team. Rather than providing access levels to every individual user, the team has decided to create groups with required access levels and add users to that groups as needed. See the following requirements:

a. Create a group named `nautilus_developers` in all App servers in `Stratos Datacenter`.

b. Add the user `rajesh` to `nautilus_developers` group in all App servers. (create the user if doesn't exist).

## Solution

a. Collect all the SSh credentitals for all the servers
b. Log into the servers using SSH
c. Create a BASH script.
```
    sudo vim useradd.sh
    => sudo useradd rajesh  #create user rajesh first
    => sudo groupadd nautilus_developers  #create group nautilus_developer
    => sudo usermod -a -G nautilus_developers rajesh  #add user to the group
```
d. Execute the script in all the specified servers
```
  sudo bash useradd.sh
```
