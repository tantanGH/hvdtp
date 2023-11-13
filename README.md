# HVDTP.X

A simple high memory VDT/V16 movie player for Human68k/X680x0

---

## About This

ハイメモリ専用のVDT/V16動画プレーヤです。

 - fpsを優先するため逐次読み込み再生ではなくすべてハイメモリに一括バッファ
 - 7つの表示モードをサポート (再生中にF1~F7で切り替え可能)
 - 15kHz/31kHzモード両対応
 - リピート再生対応 
 - PCMドライバとしてPCM8A.X / PCM8PP.X を使用

当時物のVDT/V16プレーヤーソフトはPhantomXライトバックモードで正常に動作しないものが多いのと、当時存在し得なかったハイメモリフルバッファリングでの再生を試してみたかったので作成しました。

MCSEL.X と組み合わせての利用を推奨します。

---

## 動作環境

* PhantomX 1.03d 以降 ライトバックモード推奨
* 68030モード ハイメモリ768MB推奨
* TS16DRVp.X ハイメモリドライバ
* VDISK必須 (HDS非対応)
* MercuryUnit 推奨

---

## 使い方

PCM8A.X または PCM8PP.X をあらかじめ常駐させておきます。

        usage: hvdtp [options] <movie-file(.vdt|.v16)>
        options:
              -l[n]         ... リピート回数指定。数字省略で無限リピート。(0:endless, 1:default)
              -s<1-7>       ... 画面表示モード (1:default)
              -c<15|31>     ... 15/31kHz mode (15:default)
              -y<n>         ... view height (1-120, 120:default)
              -q            ... quiet mode
              -h            ... show help message

---

## 画面表示モード

1 ... 中央に128x120のサイズで表示します。

2 ... 左上と右下に128x120のサイズで表示します。

3 ... 右上と左下に128x120のサイズで表示します。

4 ... 左上と右と左下に128x80のサイズで表示します。

5 ... 左上、右上、左下、右下に128x60のサイズで表示します。

6 ... 256x240に拡大して1ライン飛ばして表示します。

7 ... 256x120のサイズで表示します。

再生中にF1~F7で切り替えることもできます。
一部のモードで画像クロップされるのは PhantomX + RP4B + S32 + 30fps コマ落ち無し再生できる限界付近を狙って調整しているためです。

---

## History

* 0.3.1 (2023/11/13) ... 画面モード追加変更
* 0.3.0 (2023/11/12) ... 初版
