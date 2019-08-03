# System3 for SDL2

武田俊也さんの [System3 for Win32](http://takeda-toshiya.my.coocan.jp/alice/) をSDL2に移植して、emscriptenでコンパイルできるようにしたものです。
System3 for Win32は一部のゲームで専用の実行ファイルを生成します（[オリジナルのreadme](https://github.com/kichikuou/system3-sdl2/blob/master/readme.txt)参照）が、SDL2版は今のところSYSTEM3汎用版のみ対応しています。

## ビルド方法

[CMake](https://cmake.org/) が必要です。

必要なライブラリ (SDL2, SDL_ttf) をインストールして、

    $ mkdir out
    $ cd out
    $ cmake -DCMAKE_BUILD_TYPE=Debug ../src/
    $ make && make install

でコンパイル・インストールできます。

Emscripten版を実行するには、[鬼畜王 on Webのリポジトリ](https://github.com/kichikuou/web)をチェックアウトして、`docs`ディレクトリに `out/system3.*` をすべてコピーしてください。
