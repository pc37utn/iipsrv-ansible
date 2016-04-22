# iipsrv-ansible

Set up an instance of [IIPImage](http://iipimage.sourceforge.net/) to serve
images according to the [IIIF standard](http://iiif.io/).

0. install [Ansible] and [Git]
1. `git clone https://github.com/umd-mith/iipsrv-ansible.git`
2. `cd iipsrv-ansible`
2. edit `hosts` to point at your server: e.g. `images.example.org`
3. edit `iip_server_name` in `group_vars/all/config.yml` to be the same: e.g. `images.example.org`
3. `ansible-playbook iipsrv.yml`
4. put a pyramidal tiff image in `data`: e.g. `test.tif`
5. `ansible-playbook sync.yml`
6. go to http://images.example.org/iiif-image/test.tif

[Ansible]: https://www.ansible.com/
[Git]: https://github.com/trevormunoz/automation/tree/master/iiif-server
