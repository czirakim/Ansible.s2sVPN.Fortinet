<snippet>
  <content>

## Ansible.s2sVPN.Fortinet

The scope of this project is to automate the process of building 
<br>site-to-site vpn's on Fortinet firewalls.
<br>
 

## Usage

The project is made of 2 var files and a playbook. VarsA file is for siteA and varsB is for siteB.
<br> This file contains everyting that is needed to establish the vpn: 
<br>pre-shared-key, DH group, peer IP, the phase1 and phase2 proposal (i've used the same one for both),
<br>local/remote site name, local/remote subnets.
<br>The playbook contains all the tasks for creating the vpn, policies, routing and showing the status of the vpn.
<br>If you need to configure only one side you can use varsA file , and if you need to configure the other end too,
<br>you will need to run again the playbook but this time with varsB file.  
<br>
<br>Example:
<br>ansible-playbook  vpn-setup.yml -e "vars=varsA" 
<br>ansible-playbook  vpn-setup.yml -e "vars=varsB"


## Credits
This was written by Mihai Cziraki
</content>
</snippet>
