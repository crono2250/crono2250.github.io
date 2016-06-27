---
layout: single
type: posts
title: FlexCore4全体構成(こっちは非公開)
read_time: true
comments: true
share: true
related: true
---

![alt]({{ site.url }}{{ site.baseurl }}/images/FC4_All.png)

# FlexCore4 CNCコントローラシステム
 FlexCore4は、4つの要素で構成されています。
 Windows上で動作する制御ソフトウェアで全体のコントロールを行います。

 - 制御ソフトウェア

    FC4の全体を制御するソフトウェアです。
    動作パラメータの初期設定、Gコードの読み込み、軸のマニュアル操作、I/Oの操作等を行います。

    Windows上で動作し、USB経由でMC,SEQと接続します。
 
 - Motion Controller (MC)

    主に軸制御を行うコントローラです。
    円弧補間、ヘリカル補間をボード上で行い、PC側の負荷を軽減します。

 - KeyPad(KP)

    Motion Controller下に接続される操作盤です。
    軸のマニュアルコントロール(手パ)、DNC運転開始・停止、オーバライド量設定、I/Oのコントロールなど
    基本的に全ての操作をこの操作盤より行う事が出来ます。

    制御ソフトからのみ操作する場合、KPは必須ではありません。

 - Sequencer(SEQ)

    I/O接点入出力を拡張します。 FC4システムにSEQを追加していく事で、必要なI/O数を確保出来ます。
    ポンプ・照明等のON/OFF、ツールチェンジャ(ATC)のコントロール、扉開閉・温度モニタなど
    動作はユーザが定義し割り付ける事が出来ます。

    モータだけ動けばよく、I/Oが不要の場合はSEQは必須ではありません。

{% comment %}

## Motion Controller

### Motion Controller
 ほげげ

### てすとん

## KeyPad

## Sequencer


	2. I/O Port Spec

	| Pin# | Description | Type  | DIR |   | DIR | Type  | Discription | Pin# |
	|-----:|------------:|:-----:|:---:|:-:|:---:|:-----:|:------------|:-----|
	|     1|          +5V| Power |  -  |   |  -  |   -   | +5V         |2     |
	|     3|          GND| Power |  -  |   |  -  |   -   | GND         |4     |
	|     5|        X_DIR| LVTTL | OUT |   | OUT | LVTTL | X_CLK       |6     |


	| Tables        | Are           | Cool  |
	| ------------- |:-------------:| -----:|
	| col 3 is      | right-aligned | $1600 |
	| col 2 is      | centered      |   $12 |
	| zebra stripes | are neat      |    $1 |

	3. TBD_
{% endcomment %}
