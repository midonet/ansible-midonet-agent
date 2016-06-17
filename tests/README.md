Vagrantfile
===========

Before running `vagrant up`, make sure only `ubuntu` box is getting used and 
`centos` box has been commented out in Vagrantfile. The reason is, this
`ansible-midonet-agent` role depends upon `abelboldu.zookeeper` role and that
role does not have zookeeper installation steps added for RedHat. So until those
steps get added, only use `ubuntu` box for testing.
