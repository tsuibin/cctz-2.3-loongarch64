# cctz 2.3 on loongarch64

    cmake -B build -DCMAKE_INSTALL_PREFIX=$PREFIX -DCMAKE_BUILD_TYPE=Release \
          -DCMAKE_POSITION_INDEPENDENT_CODE=ON -DBUILD_TESTING=OFF .
    cmake --build build -j4 && cmake --install build

零补丁。Doris 的 `util/arrow/block_convertor.h` 需要 `cctz/time_zone.h`。
