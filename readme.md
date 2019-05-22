# ガイスター　プログラム

## 概要
これは、ボードゲームAIワークショップ第1回で、参加者のみなさまに触っていただくための「ガイスター」ゲームのサンプルプログラムです。  
* プログラムの実行にあたっては、（物理的に存在する）ガイスターのボードをはさんで相手と向き合い、交互に手を打つという想定で作っています。AIが考えた指し手は人間がボードに反映し、相手の指し手はキーボードから入力します。したがって、相手は別のAIでも、人間でもOKです。（画面にAI側のコマ色が表示されますので、画面を相手に見られてはいけません）
* 動作環境はPython 3.5以降。特別なライブラリは不要です。

## リポジトリの内容
このリポジトリには、次のファイルがあります。
* GeisterWorkshop.py : 手元のPythonで実行する場合にはこのコードを使ってください。
* GeisterWorkshop.ipynb : Google Colaboratoryで作ったファイルです。手元のマシンにPythonがなくても、open in Colabをクリックすることで、Google Colaboratiroryで開き、実行することができます。詳しいプログラムの解説もこのファイルに書いてあります。

## AIの行動を変更するためにすぐやれる、いくつかのこと。

1. 375、376行目  
初期配置を変更しましょう。COL_RとCOL_Bの配置を工夫してください。
1. 758行目  
「赤コマ3個捕獲したら、もうコマを取らなくなる」の数字を2とか1とか、場合によっては4に変更してもいい（4個とってすぐ負けることになるかも、だけど）。
1. コマ色推定機能を組み込んでみる  
たとえば「20手目までに動いた敵コマは全部赤」と仮定して、それらのコマのe_colorにCOL_Rを入れてしまうコードを、754行目あたりに組み込んでみるとどうでしょう。
1. 相手のコマ色推定機能の逆を行く  
上の対策で「赤コマだけで攻める」作戦が不利になったら、今度はそこを変更しましょう。762行目「20手までは赤コマだけで攻める」の20を変更。0でもいいし100でもいい。763行目のCOL_RをCOL_Bにかえて「n手目までは青コマだけで攻める」と逆にしてしまう手もあり？
1. ほかにも  
より良いコマ色推定、最短ルート探索、自陣を守るための方策、敵をだますためのテクニック、捕獲したいコマに向かって移動する方法など、いくらでもやれることはあります。良い方法を思いついたら、やってみましょう。


## ライセンス
GPLv3  
© Morikatron Inc. 2019  
written by matsubara@morikatron.co.jp  
