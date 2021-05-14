# Packer

This role permit to discover Packer.

Do the command to execute the playbook: ansible-playbook Run-Packer.yml

The playbook Install_Packer.yml will:

	- First it will install Packer from the official Linux repository;
        - Secondly, it will update and upgrade your host;
	- Next, it will installer Packer and virtualbox;
	- Finally, it will print the Packer's version.

The playbook Create_Image.yml will:

	- Firt, create the directory for packer and the other directory in /opt/packer;
	- Secondly, it will copy the preseed.cfg and tempalte ubuntu.json on the host;
	- Next, it will download the ubuntu iso if it doesn't exists;

Finally, when the playbook has finished, execute the command packer build ubuntu.json to create the VM.

Go to /opt/packer and do the command ls to see all the repository and you will see an output-virtualbox-iso directory.

Execute virtualbox and import the ubuntu.ova start the VM.
