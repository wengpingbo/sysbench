# Cross compile in Android

mkdir out
./autogen.sh
ac_cv_func_malloc_0_nonnull=yes ./configure --prefix=`pwd`/out CFLAGS="-static -fPIE" LDFLAGS="-static -fPIE -pie" --without-mysql CC=/path/to/aarch64-linux-android-gcc --host=aarch64-linux
make -j8
make install
