# iipimage-ansible

Set up an instance of [IIPImage](http://iipimage.sourceforge.net/) to serve images according to the [IIIF standard](http://iiif.io/).

## To Run

1. `git clone https://github.com/umd_mith/iipimage-ansible.git`
3. edit `hosts` to point at your server
4. supply the domain name for your server in `config.yml`
5. `ansible-playbook -v iipimage.yml`

## Notes

This setup expects pyramidal tiff images to be located on the server at `/data`
