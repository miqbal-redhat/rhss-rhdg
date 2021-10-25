# rhss-rhdg

This directory only contains the relevant file(s) and directories so make sure you perform relavant operations as described in order to build binaries or setup the cluster

#Build  binaries
RHSSO binaries are placed in the binaries directory under build script directory and properties file is madified according to your file system and versions

# To start RHSSO node1
1. RHSSO binary is unpackaged and relevant files are replaced 
2. A user is added  or simply RHSSO binariy is built by executing build script
./rhsso/node1/rh-sso-7.5/bin/standalone.sh -server-config=standalone-ha.xml --properties=properties/rhsso-cluster-eu-01.properties

# To start RHSSO node2
1. RHSSO binary is packaged and relevant files are replaced 
2. A user is added  or simply RHSSO binariy is built by executing build script
./rhsso/node2/rh-sso-7.5/bin/standalone.sh -server-config=standalone-ha.xml --properties=properties/rhsso-cluster-eu-01.properties

# To start RHDG site1
1. RHDG binary is unpackaged and relevant files are replaced 
2. A user is added
  bin/cli.sh user create admin -p "password!"
3. Now the site can be started
./rhdg/site1/redhat-datagrid-8.1.0-server/bin/server.sh -c infinispan.xml


# To start RHDG site2
1. RHDG binary is unpackaged and relevant files are replaced 
2. A user is added
  bin/cli.sh user create admin -p "password!"
3. Now the site can be started
./rhdg/site2/redhat-datagrid-8.1.0-server/bin/server.sh -c infinispan.xml -o 100
