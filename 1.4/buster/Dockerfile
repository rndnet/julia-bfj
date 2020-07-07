FROM julia:1.4-buster
RUN apt-get update  && apt-get install -y python3 python3-pip && \
    pip3 install -r https://server1.rndnet.net/static/simple/bfj/requirements.txt && pip3 install --index-url https://server1.rndnet.net/static/simple bfj && rm -rf /var/lib/apt/lists/* && \
    julia -E 'import Pkg;Pkg.add(Pkg.PackageSpec(url="https://gitlab.com/rndnet/apps/BFJ.jl",rev="master"))' 
