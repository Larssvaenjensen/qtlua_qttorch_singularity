bootstrap: docker
from: nvcr.io/nvidia/torch:18.08-py2

%post
    echo "start" 
    apt-get -y update
    echo "1" 
    git clone https://bitbucket.org/mchldann/aaai2019.git
    cd aaai2019/
    echo "2" 
    apt-get install -y libsdl1.2-dev libsdl-gfx1.2-dev libsdl-image1.2-dev cmake
    mkdir build && cd build
    cmake -DUSE_SDL=ON -DUSE_RLGLUE=OFF -DBUILD_EXAMPLES=ON ..
    make -j 4
    echo "3" 
    cd ..
    pip install .
    echo "4" 
    cd src/agent
    chmod +x run_gpu_pellet
    echo "5" 
    apt install -y qt4-default
    luarocks install qtlua
    luarocks install qttorch
    luarocks install lanes
    echo "slut" 
    
