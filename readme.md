# KOJS-Agent
KOJSの問題に対する答案コードの実行管理をするプログラム群です.

## 対応言語一覧表
対応準備中: ToDo / 今後対応予定: TBD

| 言語名        | 処理系名    | 言語ID    | 大まかなバージョン | 備考/メモ　    |
|------------|---------|---------|-----------|-----------|
| C          | GCC     | GCC     | v9以降？     | 12系に固定したい |
| C          | Clang   | Clang   | ?         |           |
| C++        | G++     | C++     | ?         |           |
| C++        | Clang++ | Clang++ | ?         |           |
| Ruby       | CRuby   | Ruby    | 3.x.x     | YJIT導入?   | 
| Python     | CPython | Python3 | 3.x.x     |           | 
| Go         | Go(gc)  | Go      | 1.20.x    |           |
| Rust       | rustc   | Rust    | ToDo      |           |
| Java       | OpenJDK | OJDK    | ToDo      |           |
| JavaScript | Node.js | Node    | ToDo      |           |
| TypeScript | tsc     | TSC     | TBD       | 優先度低め     |

- ※ 備考
  - Workerが対応している言語でも実行できない場合があります

## 実行環境情報
- 実行はすべてDockerコンテナ上で行われます
- 実行コンテナのOSは基本的にDebian(Bullseye)に設定しています
- ホストのアーキテクチャはamd64(x86_64)/AArch64(Arm64,apple M1)で動作確認を行っています
  - ただし、実行する言語によっては結果に差異が生じる可能性があります。
- 言語のバージョンは固定されていません。イメージビルド時にaptのデフォルトのバージョンがインストールされるものが多いです。
