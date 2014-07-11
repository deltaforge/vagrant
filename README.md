vagrant
=======

Kickstart files to create custom CentOS vagrant boxes automatically.


create a box
======
Download a Centos is from one of the mirrors, eg:
- CentOS-6.5-x86_64-netinstall.iso 
- CentOS-7.0-1406-x86_64-NetInstall.iso

Create a virtualbox machine with at least 8GB disk and boot from iso.

When you're welcomed by the CentOS installation screen, hit TAB and append:

    text ks=https://raw.githubusercontent.com/deltaforge/vagrant/master/kickstart/centos7.cfg

or

    text ks=https://raw.githubusercontent.com/deltaforge/vagrant/master/kickstart/centos6-ga.cfg
  
After the kickstart is completed, package the box, e.g.:

    vagrant package --base centos7 --output centos7-latest.box
    
