git clone https://github.com/J-J-CH/depends.git

#安装gflags
cd gflags
mkdir build && cd build
cmake .. -DGFLAGS_NAMESPACE=google -DCMAKE_CXX_FLAGS=-fPIC ..
make -j4
sudo make install
sudo ldconfig

#安装glog
cd glog
mkdir build && cd build
cmake -DGFLAGS_NAMESPACE=google -DCMAKE_CXX_FLAGS=-fPIC -DBUILD_SHARED_LIBS=ON ..
make -j4
sudo make install
sudo ldconfig

#安装yaml-cpp
cd yaml-cpp
mkdir build && cd build
cmake -DBUILD_SHARED_LIBS=ON ..
make
sudo make install
sudo ldconfig
