Bootstrap: docker
From: centos:7

%post
    echo "Updating packages..."
    yum clean all; yum -y update

    echo "Installing some needed things..."
    yum -y install which # needed by NSC compiler wrapper
    
    echo "Installing group Development Tools..."
    yum -y groupinstall 'Development Tools'

    echo "Installing CentOS IB stack..."
    yum -y install dapl dapl-utils ibacm infiniband-diags libibverbs libibverbs-devel libibverbs-utils libmlx4 librdmacm librdmacm-utils mstflint opensm-libs perftest qperf rdma

    echo "Creating NSC mount points..."
    umask 0022
    mkdir -p /scratch/local
    mkdir -p /software
