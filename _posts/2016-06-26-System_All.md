---
layout: single
type: posts
title: FlexCore4全体構成
read_time: true
comments: true
share: true
related: true
---

![alt]({{ site.url }}{{ site.baseurl }}/images/FC4_All.png)

# FlexCore4 CNCコントローラシステム
 FlexCore4は、大きくわけて3つのモジュールで構成されています。
 - Motion Controller (MC)
    主に軸制御を行うコントローラです。
    円弧補間、ヘリカル補間をボード上で行い、PC側の負荷を軽減します。

 - KeyPad(KP)
    Motion Controller下に接続される操作盤です。
    軸のマニュアルコントロール、DNC運転開始・停止、オーバライド量設定、I/Oのコントロールなど
    基本的に全ての操作をこの操作盤より行う事が出来ます。

 - Sequencer(SEQ)
    I/O接点入出力を拡張します。 FC4システムにSEQを追加していく事で、必要なI/O数を確保出来ます。
    ポンプ・照明等のON/OFF、ツールチェンジャ(ATC)のコントロール、扉開閉・温度モニタなど
    動作はユーザが定義し割り付ける事が出来ます。

## Motion Controller

### Motion Controller
 ほげげ

### てすとん

## KeyPad

## Sequencer


{% comment %}
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
