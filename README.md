	1. Launch 2 Amazon Linux Ec2 instance (Master-Server & Slave-Server); Enable Auto Assign Public IP, Set your SG open all
	2. Ssh into the Master Server
	3. Install Ansible (sudo amazon-linux-extras install ansible2) or sudo amazon-linux-extras install ansible2 -y
	4. Ansible version
	5. Sudo Su
	6. Create a .pem file (vi testposi.pem)
	7. On your cli; cat into your key pair
	8. cat testposi.pem
	9. Copy the content of your keypair & paste to your testposi.pem file on your master-server. Ensure you remove the %. On the pem file
	10. ls -al
	11. Chmod 400 tesposi.pem
	12. Ssh into the slave server
	13. Ssh ec2-user@<private ip of slave master> -i testposi.pem
	14. .
	15. .
	16. In the Master Server
	17. Sudo su
	18. Mkdir my-playbook
	19. Cd my-playbook
	20. Vi inventory.ini and paste the below
	21.  172.31.2.78 ansible_user=ec2-user ansible_ssh_private_key_file=testposi.pem ansible_connect=ssh
	22. In your my-playbook folder you now have a testposi.pem and inventory.ini files
	23. # ansible all -m ping -i inventory.ini or ansible webservers -m ping -i inventory.ini
	24. Create another file 
	25. Vi playbook.yml
	26. Write the below playbook to install httpd in the slave server
	- na
	- 

1. To test the play
2. # ansible-playbook playbook.yml -i inventory.ini
3. Copy the slaver server public ip and search on internet to check what it brings out
4. Create an html page (a developer writes the html code for u to lunch) update your inventory to run this html
5. # vi index.html
6. 
7. Vi playbook.yml



# ansible-playbook playbook.yml -I inventory.ini --check
# ansible-playbook playbook.yml -I inventory.ini

Copy the public ip of the slave server and search 



![image](https://github.com/Lordcarter/mytest-playbook/assets/135546990/7d26782a-797e-4dc8-9cf3-3b027ffce218)
