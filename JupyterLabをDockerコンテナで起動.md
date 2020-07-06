0. (Dockerインストールしてない場合) Dockerのインストール  
   起動->鯨のコンテナが動き出し、その動きが止まったら準備OK

1. 適当な場所にyamlファイル（後述）とworkディレクトリ作成  
   workファイルにはコンテナ内で動くjupyterlabのフォルダがマウントされる  
   [docker-compose.ymlの中身](docker-compose.yml)

2. yamlファイル、workディレクトリと同じディレクトリで次の2つのコマンドを実行  
   2.1  `docker-compose build` // dockerImage を作成している
   2.2  `docker-compose up`    // コンテナの軌道から立ち上げまで  
   2.3  2.2実行時、画面に表示されるtokenをコピーしておく  
3. ブラウザで localhost:80/ にアクセス
4. パスワードに2.3でコピーしたtokenをペースト
   画面にjupyterの画面表示されればOK

作成したコードなどファイル類は、workディレクトリに入れることで
localのworkディレクトリにも反映される（マウントの設定しているため）。
