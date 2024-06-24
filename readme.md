# Thunderbirdで、Content-Language: ja-JP にするダミー辞書
現在の Thunderbird は、日本語メールを書いても、Content-Language: en-US になってしまいます。  
調べた範囲では、現状「どのスペル辞書を使っているか」を元に Content-Language: が決定されるようです（あまり宜しくない作りですが）。  
過去に議論にはなっているようですが解決の兆しはなく、空の日本語辞書を登録するのが（暫定策として）近道のようです。
これはそのためのダミー辞書となります。

## 利用方法
1. jajp.xpiをダウンロードして、Thunderbird アドオンとテーマ → 辞書、を選んで「ファイルからアドオンをインストール」でインストール
2. 設定 → 編集 → スペルチェック → 辞書の言語で、日本語「だけ」をチェック（優先順位を指定するUIは無さそうなので）
3. メッセージ作成で「スペル」ボタンのプルダウンメニューで、日本語が選択されていることを確認

## 中身
xpiはzipですので、zipとして中身を解けば、manifest.jsonという定義ファイルと、dictionaries配下に辞書となるデータファイル群（ほぼ空）を見ることができます。

## 参考URL
https://forums.mozillazine.jp/viewtopic.php?f=3&t=17981  
https://bugzilla.mozilla.org/show_bug.cgi?id=1678812
