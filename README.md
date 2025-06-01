wsl --install 
sudo apt update
sudo apt install ansible -y 
sudo apt update wsl
ansible --version
mkdir p7
cd p7
wsl
nano inventory
	[local] 
	localhost ansible_connection=local
	Ctrl+S, Ctrl+X
nano playbook.yml
	- name: Experiment 7 - Run Task on Localhost 
	  hosts: local 
	  tasks: 
		- name: Print Hello 
		 debug: 
		    msg: "Hello from Ansible on Windows via WSL!"
		Ctrl + S to Save ; Ctrl + X 
ansible-playbook -i inventory playbook.yml 
