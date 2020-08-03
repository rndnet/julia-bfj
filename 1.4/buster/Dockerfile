FROM julia:1.4-buster
RUN apt-get update  && apt-get install -y unzip python3 python3-pip && \
    pip3 install -r https://server1.rndnet.net/static/simple/bfj/requirements.txt && pip3 install --index-url https://server1.rndnet.net/static/simple bfj && rm -rf /var/lib/apt/lists/* && \
    julia -E 'import Pkg;Pkg.add(Pkg.PackageSpec(url="https://gitlab.com/rndnet/apps/BFJ.jl",rev="master"))' && \
    julia -E 'import Pkg;Pkg.add("HDF5"); Pkg.add("Plots"); Pkg.add("Dierckx");Pkg.add("FFTW");Pkg.add("SpecialFunctions");Pkg.add("Convex");Pkg.add("ECOS");Pkg.add("Interpolations");Pkg.add("PyCall")' &&\
    julia -E 'import Pkg;Pkg.add("LinearAlgebra"); Pkg.add("Statistics");'
