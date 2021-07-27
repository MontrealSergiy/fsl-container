Bootstrap: docker
From: ubuntu:20.04
%post
    apt-get update
    apt-get install -y bc
    apt-get install -y wget
    apt-get install -y python
    apt-get install -y libgl-dev
    apt-get install -y libquadmath0
    wget https://fsl.fmrib.ox.ac.uk/fsldownloads/fslinstaller.py
    python fslinstaller.py -d /usr/local/fsl -V 6.0.4
    rm -rf /usr/local/fsl/src
%environment
    export FSLDIR=/usr/local/fsl
    export PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/fsl/bin
    export  LD_LIBRARY_PATH=/usr/local/fsl/lib
    export FSLOUTPUTTYPE=NIFTI_GZ
%post
    . /usr/local/fsl/etc/fslconf/fsl.sh
