#DevOps Training Bootcamp Self Contained Toolset VM


###Prerequisites:
- Install git (*https://git-scm.com/downloads*)
- Install Vagrant (*https://www.vagrantup.com/downloads.html*)
- Install Virtualbox (*https://www.virtualbox.org/wiki/Downloads*)
    - Either change to the directory that Virtualbox has been installed into (e.g. 'c:\program files\oracle\virtualbox' for Windows) or add the path to your Path variable. This is needed to run the following commands. 
    - Disable account authentication for virtualbox web server '*VBoxManage setproperty websrvauthlibrary null*'
    - Run Virtualbox web service '*vboxwebsrv -H 0.0.0.0*'
- Clone repository to local directory '*git clone https://github.com/davlloyd/devops-training-vagrant.git*'


###Get it Running:
- Change into directory repo was cloned into
- run command '*vagrant up*'
- Access guest via '*vagrant ssh*'

###Further details:
- port 5000 is redirected as 5000 on localhost for script testing
- Port 2375 is redirected as 3375 so that you can use the VMs docker engine locally (e.g SET DOCKER_HOST=tcp://localhost:3375 or same again but with EXPORT instead of SET for OSX)
- Text editors are installed in guest (VIM and Nano) but you can edit/create scripts via the <clonedir>/work directory which is mounted as /vagrant/work in the guest


###So What Is In It?:
As part of the VM the following is installed and configured
- git cli
- Python and required modules
- docker
    - engine
    - docker machine
    - RexRay (container storage volume driver)
- VIM and Nano text editors
- Pivotal CloudFoundry cli (CF)


### Notes
As part of the Vagrant install it will attempt to start the RexRay service as the last step. In this demo setup the RexRay service 


