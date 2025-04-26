# ヒューマノイド開発プラットフォーム BaseNoid
## What's BaseNoid
![BaseNoid_Overall_view](https://github.com/Sugi-kmmm/BaseNoid/blob/main/BaseNoid_Images/Overall_view.png)

　BaseNoidは，低価格で本格的なヒューマノイドロボットを開発することを目的とした，ヒューマノイド開発プラットフォームです．[東京工業大学　ロボット技術研究会](https://rogiken.org/)が所持する工作機械（CNCフライス・3Dプリンタ）のみで作成できる上，必要な機械要素の入手性もきわめて高いことが特徴です．

## ファイル構成
　このリポジトリ内のファイル構成は，以下のようになっています．
```
Top
|-LICENSE                                   ライセンス情報
|-README.md                                 本リポジトリの説明
|-BaseNoid.stp                              BaseNoidの組み立て済みCADファイル
|-BaseNoid_Images           
|   |-Overall_view.png                      BaseNoidの全体図
|
|-Making_Files                              製作に必要な展開済み板金モデル等
    |-Files_for_3DP                         3Dプリンタにより作成可能なパーツ類
    |   |-Torso                             Torso部分に必要なパーツ
    |       |-Torso_3Dprint_parts.stp 
    |
    |-Files_for_CNC_parts                   CNCフライスにより作成可能なパーツ類（部位ごとに分類）
    |   |-Arm                               Arm部分に必要なパーツ群
    |   |   |-Arm_t1.5_CAM.stp              t1.5板材から切削可能なパーツ群
    |   |   |-Arm_t3_CAM.stp                t3板材から切削可能なパーツ群
    |   |
    |   |-Leg
    |   |   |-Leg_t1.5_CAM_1.stp            t1.5板材から切削可能なパーツ群
    |   
    |       ～略～
    |
    |-Files_for_CNC_all                     CNCフライスにより作成可能なパーツ類（部位ごとの分類なし．最大200x400の板材から削りだすことを想定）
        |-Arm_Leg_Torso_Waist_t1.5_CAM.stp  Arm,Leg,Torso,Waistに使用されるt1.5パーツ群
        |-Arm_Leg_Waist_t3_CAM.stp          Arm,Leg,Waistに使用されるt3パーツ群（t2.8パーツ含む）
        |-Leg_t1.5_CAM_1.stp                Legに使用されるt1.5パーツ群
        |           
        |           ～略～
```

## 購入部品・材料
機械要素として，以下のものを購入してください．

### [MISUMI](https://jp.misumi-ec.com/)より購入

|型番|単価|個数|小計（税別）|詳細|
| --- | --- | --- | --- | --- |
| LFW-2215 | 294円 | 3 | 882円 | スラストワッシャ．スラスト摩擦を低減する部品． |
| 80F-0403 | 60円 | 4 | 240円 | フランジ付きブッシュ．ベアリングみたいなもの． |
| PSFHRW5-42.5-MD3-ND3 | 850円 | 2 | 1700円 | 両端に目ねじがついてる棒．自分で旋盤加工して作ってOK． |
| BOB-M3-2-3W | 18円 | 52 | 936円 | クレンチングナット．板に圧入する便利なナット |


### [秋月電子通商](https://akizukidenshi.com/catalog/default.aspx)より購入

|内容|単価|個数|小計（税込）|詳細|
| --- | --- | --- | --- | --- |
| FEETECHサーボ STS3215 | 2980円 | 19 | 56620円 | シリアルサーボモータ．よくあるPWMサーボとは違って，角度とか速度とか温度とかを返してくれる，賢いサーボ |

また，必要なアルミ材は以下の通りです．（Files_for_CNC_allを用いて製作した場合）

### [井田商店](https://www.idasyouten.jp/)より購入
|内容|単価|個数|小計（税別）|詳細|
| --- | --- | --- | --- | --- |
| A5052材 t1 | 280円 | 1 | 280円 | 幅40mm 長さ40mm |
| A5052材 t1.5 | 890円 | 3 | 2670円 | 幅200mm 長さ400mm |
| A5052材 t2 | 890円 | 1 | 890円 | 幅200mm 長さ350mm |
| A5052材 t3 | 670円 | 1 | 670円 | 幅200mm 長さ170mm |
| A5052材 t5 | 210円 | 1 | 210円 | 幅120mm 長さ50mm |

合計金額（税込）：**65946**円

## ACT_Base_Circuitについて
　BaseNoidでは，制御用基板としてACT_Base_Circuit（以下，ABC）というロボット技術研究会ACTで開発している多軸ロボット向け制御基板を用いています．

　ABCを使用しない場合は，[秋月電子通商様のSTS3215商品ページ](https://akizukidenshi.com/catalog/g/g116312/)内で紹介されている[参考資料](https://akizukidenshi.com/goodsaffix/feetech_digital_servo_20220729.pdf)の7ページ目をご確認の上，ご自分で回路を実装していただけましたら幸いです．

## コンタクト
　技術的お問い合わせは，本リポジトリのIssueよりお願いいたします．

　その他の問い合わせについては，[開発者HP内のコンタクトに記載された手段](https://sugi-kmmm.github.io/contact.html)により行ってください．また，教育機関の講義で使用する場合等においては，特段の連絡は必要ありませんが，ご報告していただけますと製作者のモチベーションにつながります．ぜひご一報いただけますと幸いです．

## LICENSE情報
BaseNoidは以下のクリエイティブ・コモンズ・ライセンスにより保護されています．

BaseNoid © 2025 by [Rei Sugihara](https://sugi-kmmm.github.io/collection.html) is licensed under [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/?ref=chooser-v1).