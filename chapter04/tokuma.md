## 4.1
> 図4-1でも図4-2でも主なコンポーネントにうストレージ(データ保存装置)がふくまれていません。フラッシュやディスクのようなストレージは図のどこに対応しますか？


メモリには記憶階層という概念が存在し、一次記憶と二次記憶に分かれる。一次記憶は高速かつ揮発性のあるメインメモリに対応し、二次記憶はストレージのような記憶装置が利用される。(詳細は10章)

したがってストレージはメモリの部分に対応する。


## 4-6
> フォン・ノイマンアーキテクチャがハーバードアーキテクチャよりもハッカーの攻撃に弱いといいますが、どんなところが弱いのでしょうか？

フォン・ノイマンアーキテクチャの場合、同じメモリ領域にデータと命令が格納される。そのため、命令はデータとしてメモリ上読み込まれる。メモリ上のデータが命令かどうかを判断することができないないことから、バッファーオーバーフローと呼ばれる攻撃が行われやすい。

簡単に言うとバッファオーバーフローとは、命令によって事前に確保されたメモリの範囲を超えるのデータを送りつけ、OSのセキュリティに関わる情報を書き換えてしまうような攻撃のこと。

詳しくは[こちら](https://www.ipa.go.jp/security/awareness/vendor/programmingv2/contents/c901.html)を参照

対応策としてこちらの[NXビット](https://ja.wikipedia.org/wiki/NX%E3%83%93%E3%83%83%E3%83%88)などがあるよう。