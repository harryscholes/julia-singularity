BootStrap: docker
From: ubuntu:18.04

%runscript
julia --startup-file no --history-file no

%environment
export PATH=/julia-1.2.0/bin:$PATH
export LD_LIBRARY_PATH=/julia-1.2.0/lib:/julia-1.2.0/lib/julia:$LD_LIBRARY_PATH
export LC_ALL=C

%post
apt-get -y update
apt-get -y install curl
curl -L "https://julialang-s3.julialang.org/bin/linux/x64/1.2/julia-1.2.0-linux-x86_64.tar.gz" | tar xz
apt-get -y purge curl
apt-get clean
apt-get -y autoremove
