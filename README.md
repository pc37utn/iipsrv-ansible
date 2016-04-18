# iipimage-ansible

Set up an instance of [IIPImage](http://iipimage.sourceforge.net/) to serve
images according to the [IIIF standard](http://iiif.io/).

1. `git clone https://github.com/umd_mith/iipimage-ansible.git`
2. edit `hosts` to point at your server: e.g. `images.example.org`
3. `ansible-playbook iipimage.yml`
4. put a pyramidal tiff image in `data`: e.g. `test.tif`
5. `ansible-playbook sync.yml`
6. go to http://images.example.org/iiif-image/test.tif
