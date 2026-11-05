# cctz 2.3 on loongarch64

    cmake -B build -DCMAKE_INSTALL_PREFIX=$PREFIX -DCMAKE_BUILD_TYPE=Release \
          -DCMAKE_POSITION_INDEPENDENT_CODE=ON -DBUILD_TESTING=OFF .
    cmake --build build -j4 && cmake --install build

零补丁。Doris 的 `util/arrow/block_convertor.h` 需要 `cctz/time_zone.h`。

## 更新（2026-11-04）

`util/arrow/block_convertor.h` 在最终 BE 编译中正常找到 `cctz/time_zone.h`，全量链接通过。
