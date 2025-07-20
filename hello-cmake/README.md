编译步骤（基于Debian12）

```sh
# 安装前置环境
apt -y install cmake gcc

cd hello-cmake

# 将编译的内容全部放置到gaga目录。
# DCMAKE_INSTALL_PREFIX与autotools中的prefix一致，默认为/usr/local
cmake -B gaga -DCMAKE_BUILD_TYPE=Release -DCMAKE_INSTALL_PREFIX=$PWD/install
# 编译gaga目录
cmake --build gaga
# 将gaga目录的内容，移植到CMAKE_INSTALL_PREFIX
cmake --install gaga

# 验证
./install/bin/hello

```