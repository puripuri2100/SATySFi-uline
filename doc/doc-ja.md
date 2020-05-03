下線を引くコマンドと関数を提供するパッケージです。

モジュール名は`Uline`です。

# 提供コマンド

- `\uline`：単純な下線
- `\uuline`：2重下線
- `\sout`：打ち消し線
- `\dashuline`：ダッシュの下線
- `\dotuline`：点線
- `\uwave`：波線

全て型は`[color?; inline-text] inline-cmd`となっている。

色を指定しない場合はcontextに保持されているtext-colorの値が採用されるが、色を指定すればその色で描画される。

# 提供関数

- `make-uline`：単純な下線
- `make-uuline`：2重下線
- `make-sout`：打ち消し線
- `make-dashuline`：ダッシュの下線
- `make-dotuline`：点線
- `make-uwave`：波線

全て型は`length -> color -> deco-set`となっている。

第一引数は太さの情報で、第二引数は色の情報である。
返ってきたdeco-setoを`inline-frame-breakable`で処理してほしい。
