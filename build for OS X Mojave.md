git clone https://github.com/davembg/Zealium.git

cd Zealium
sh autogen.sh

./configure --disable-tests --disable-dependency-tracking --with-gui=qt5 --with-boost=/usr/local/opt/boost --with-boost-libdir=/usr/local/opt/boost/lib \
--with-boost-system=boost_system-mt --with-boost-filesystem=boost_filesystem-mt \
CXXFLAGS="-pipe -O2 -std=c++11 -isysroot /Applications/Xcode.app/Contents/Developer/Platforms/MacOSX.platform/Developer/SDKs/MacOSX10.11.sdk \
-mmacosx-version-min=10.11 -Wno-unused-variable -Wno-unused-parameter -fPIC -I/usr/local/opt/openssl/include -I/usr/local/opt/boost/include " \
LIBS="$LIBS -L/usr/local/opt/openssl/lib -lssl" \
SSL_CFLAGS=-I/usr/local/opt/openssl/include CRYPTO_CFLAGS=-I/usr/local/opt/openssl/include \
SSL_LIBS=-L/usr/local/opt/openssl/lib CRYPTO_LIBS=-L/usr/local/opt/openssl/lib

make V=1
make deploy
