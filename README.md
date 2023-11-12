# HVDTP.X

A simple high memory VDT/V16 movie player for Human68k/X680x0

---

## About This

ハイメモリ専用のVDT/V16動画プレーヤです。

 - fpsを優先するため逐次読み込み再生ではなくすべてハイメモリに一括バッファ
 - 5つの表示モードをサポート
 - 15kHz/31kHzモード両対応
 - リピート再生対応 
 - PCMドライバとしてPCM8A.X / PCM8PP.X を使用

MCSEL.X と組み合わせての利用を推奨します。

---

## 動作環境

* PhantomX 1.03d 以降 ライトバックモード推奨
* 68030モード ハイメモリ768MB推奨
* TS16DRVp.X ハイメモリドライバ
* VDISK
* MercuryUnit 推奨

---

## History

* 0.3.0 (2023/11/12) ... 初版
