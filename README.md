# iipsrv-ansible

Set up an instance of [IIP Image Server (iipsrv)](http://iipimage.sourceforge.net/) on RHEL to serve images and their metadata using [IIIF](http://iiif.io/). 

0. install [Ansible] and [Git]
1. `git clone https://github.com/umd-mith/iipsrv-ansible.git`
2. `cd iipsrv-ansible`
2. edit `hosts` to point at your server: e.g. `images.example.org`
3. edit `iip_server_name` in `group_vars/all/config.yml` to be the same: e.g. `images.example.org`
3. `ansible-playbook iipsrv.yml`
4. put a pyramidal tiff image in `data`: e.g. `test.tif`
5. `ansible-playbook sync.yml`
6. go to http://images.example.org/iiif-image/test.tif

If you'd prefer to test things locally with [Vagrant] you should be able to simply:

0. `vagrant up`
1. go to http://192.168.33.12/

[Ansible]: https://www.ansible.com/
[Git]: https://github.com/trevormunoz/automation/tree/master/iiif-server
[Vagrant]: https://www.vagrantup.com/ 
