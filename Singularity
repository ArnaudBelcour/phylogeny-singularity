Bootstrap: docker
From: ubuntu:18.04

%environment
     export PATH="$PATH:/programs/iqtree-2.0-rc1-Linux/bin:"
     export PATH="$PATH:/programs/raxml:"
     export PATH="$PATH:/programs/beast/BEASTv1.10.4/bin:"
     export LD_LIBRARY_PATH=/programs/beagle/lib:$LD_LIBRARY_PATH

%post
     apt-get -y update && \
     DEBIAN_FRONTEND=noninteractive apt-get install -y wget \
     make \
     gcc \
     flex \
     bison \
     libgmp3-dev \
     unzip \
     build-essential \
     autoconf \
     automake \
     libtool \
     pkg-config \
     openjdk-8-jdk \
     git ;\
     mkdir /programs;\
     cd /programs;\
     mkdir raxml beast beagle;\
     wget https://github.com/Cibiv/IQ-TREE/releases/download/v2.0-rc1/iqtree-2.0-rc1-Linux.tar.gz;\
     tar xzf iqtree-2.0-rc1-Linux.tar.gz;\
     git clone --depth=1 https://github.com/NBISweden/MrBayes.git;\
     cd MrBayes;\
     ./configure;\
     make && make install;\
     cd ../raxml ;\
     wget https://github.com/amkozlov/raxml-ng/releases/download/0.9.0/raxml-ng_v0.9.0_linux_x86_64.zip;\
     unzip raxml-ng_v0.9.0_linux_x86_64.zip ;\
     rm raxml-ng_v0.9.0_linux_x86_64.zip;\
     cd ../beast;\
     wget https://github.com/beast-dev/beast-mcmc/releases/download/v1.10.4/BEASTv1.10.4.tgz;\
     tar xzf BEASTv1.10.4.tgz;\
     rm BEASTv1.10.4.tgz;\
     cd ../beagle ;\
     git clone --depth=1 https://github.com/beagle-dev/beagle-lib.git;\
     cd beagle-lib;\
     ./autogen.sh;\
     ./configure --prefix=/programs/beagle;\
     make install;\
     make check ;\
     cd ../.. ;\
     rm iqtree-2.0-rc1-Linux.tar.gz;\

