# To Build on osx
```bash
brew install openssl automake

./bootstrap.sh

CXX="clang++ -std=c++11" LDFLAGS="-L/usr/local/opt/openssl/lib" \
CFLAGS=-I/usr/local/opt/openssl/include CPPFLAGS=-I/usr/local/opt/openssl/include CXXFLAGS=-I/usr/local/opt/openssl/include \
./configure --disable-gen-erl --disable-gen-hs --without-ruby --without-haskell \
--without-erlang --without-csharp --without-python --without-php --without-go \
--without-perl --enable-gen-rb=no --enable-gen-as3=no --enable-gen-csharp=no \
--enable-gen-perl=no --enable-gen-php=no --enable-gen-st=no --enable-gen-ocaml=no \
--enable-gen-xsd=no --enable-gen-html=no --enable-gen-go=no

make
```
