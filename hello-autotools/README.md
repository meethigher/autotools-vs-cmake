编译步骤（基于Debian12）

```sh
# 安装前置环境
apt -y install autoconf make gcc

cd hello-autotools
# 生成 configure
chmod +x autogen.sh && ./autogen.sh
# prefix指定编译后的安装目录。默认是/usr/local
./configure --prefix=$PWD/install
make && make install

# 验证
./install/bin/hello
```