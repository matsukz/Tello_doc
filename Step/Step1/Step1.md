# #1 ドローンを飛ばしてみよう
Python コマンドライン上でドローンを操作してみよう<br>
- [#1 ドローンを飛ばしてみよう](#1-ドローンを飛ばしてみよう)
  - [#1-1 プログラムの準備](#1-1-プログラムの準備)
  - [#1-2 PCをドローンと接続する](#1-2-pcをドローンと接続する)
  - [#1-3 ドローンを操作してみよう](#1-3-ドローンを操作してみよう)
  - [#1-4 プログラムを終了する](#1-4-プログラムを終了する)


## #1-1 プログラムの準備
* プログラム`Tello_step1.py`を開きプログラムの流れを確認しましょう
  * プログラムの意味を理解しコメントを追加してメモしておいてもいいです
  * `#`を先頭につけるとプログラムとして反映されません
      ```python
      # ドローンのアドレスを指定する
      tello_address = ('192.168.10.1', 8889)
      ```
* プログラムの意味が理解できたら実際に飛ばしてみよう
  
## #1-2 PCをドローンと接続する
* ここは何回も使うので覚えておきましょう
1. ドローンの電池をセット
   * 電池をセットする場所にドローンのIDが記載されています  
      ```
      TELLO-XXXXX
      ```
2. 電源を投入
   * サイドにある電源ボタンを１回押すと電源が入ります
   * `黄色ランプが点滅`するまで待機です
3. PCと接続
   1. Wi-Fiの設定から先程確認したドローンのIDを選択し`接続`をクリック
   2. セキュリティや`インターネットなし`といった警告が表示されますが、全部無視します
   3. 接続が完了したら次のステップへ
4. プログラムの実行
   1. `Tello_step1.py`を開いたVSCodeで上部にある`実行`の中から`デバッグの開始`を選択
   2. `Python ファイル`を選択
   3. 以下の内容が出力されれば準備完了です
      ```
      Tello Python3 Demo.

      Tello: command takeoff land flip forward back left right
            up down cw ccw speed speed?

      end -- quit demo.

      ```
## #1-3 ドローンを操作してみよう
* ドローンのインジケータランプが`黄色点滅`なことを確認してください
* ドローンとプログラムをつなげるコマンド
  ```
  command
  ```
  * ドローンのインジケータランプが`緑`になれば準備完了です
  * コマンドを入力しドローンを操作してみよう。以下は例です。
* 離陸
  ```
  takeoff
  ```
* 着陸
  ```
  land
  ```
* 時計回りにX度回転
  ```
  cw X
  ```
  `XXX`に1から3600の数値を入れる
* コマンドの例
  |コマンド|内容|
  |:---:|:---:|
  |up XX|XXcm上昇|
  |down XX|XXcm下降|
  |left XX|XXcm左へ|
  |right XX|XXcm右へ|
  |forward XX|前方にXXcm|
  |back XX|後方にXXcm|
  |cw XX|時計回りにXX度回転|
  |ccw XX|反時計回りにXX度回転|


## #1-4 プログラムを終了する
```
end
```
* ドローンが着陸していることを確認してください