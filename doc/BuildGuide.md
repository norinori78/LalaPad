# ビルドガイド

　
## 準備
### キット内容物の確認

| 名前 | 数 |
|:-|:-|
|PCB（左右＋Dpad基板）|1式|
|トラックパッドモジュール|1個|
|Dパッドモジュール用カバー|1式|
|マイクロスイッチ|4個|
|ロータリーエンコーダー|2個|
|エンコーダーノブ|2個|
|ホットスワップソケット|48個|
|FFCケーブル12PIN|1個|
|FFCケーブル5PIN|1個|
|キーボードケース|1式|
|電源スイッチカバー|2個|
|マイコンカバー＆リセットピン|2個|
|マグネット|8個|
|メタルプレート|2個|
|M3ネジ|8本|

### 別途ご用意いただくもの

| 必須 | 名前 | 数 | 備考 |参考商品|
|:-|:-|---:|:-|:-|
|★|Seeed Studio XIAO nRF52840 |2個|マイコン本体。安価で入手性が高く、通信も安定しています。|[秋月電子](https://akizukidenshi.com/catalog/g/g117341/)|
|★|Kailh Choc V2互換スイッチ|48個|個人的にDeepSeaMiniがおすすめ。Lofreeなども適合。ChocV1も一応刺さります。|[遊舎工房](https://shop.yushakobo.jp/collections/all-switches/Kailh-Choc-V2%E3%82%B9%E3%82%A4%E3%83%83%E3%83%81) [Kailhswitch](https://kailhswitch.net/products/kailh-deep-sea-silent-min-low-profile-keyboard-switch)|
|★|MX軸ロープロファイルキーキャップ|48個|MX軸なら通常キーキャップも一部適合。|[Womier](https://www.amazon.co.jp/stores/page/90526727-85E5-4BF8-AAD2-FC8A78C07BE3/search?ref_=ast_bln&store_ref=bl_ast_dp_brandLogo_sto&terms=%E3%83%AD%E3%83%BC%E3%83%97%E3%83%AD)|
|★|3.7Vリチウムポリマーバッテリー|2個|厚さ6.3mm以下、ソケットのピッチ2.0mm　※ソケットの極性に注意！|[Amazon](https://www.amazon.co.jp/dp/B08FD39Y5R/)|
|★|USB-Cケーブル|2本|充電、ファームウェア書き込み用。何百回と抜き差しする事になるのでマグネット式がおすすめ。||
||ケースの滑り止め|1式|グリップラスが評判良いです。テントするなら不要。|[Amazon](https://www.amazon.co.jp/dp/B08C9Z2K4C/])
||テンティング用品|2セット|マグネット式スタンドor三脚orクランプアーム。テントしないなら不要。|[Cramp](https://www.amazon.co.jp/dp/B08LCZ2X7M/) [Magnet](https://www.amazon.co.jp/dp/B0CXPR9BMF/) [Stand1](https://www.amazon.co.jp/dp/B0DKFMLWFX/) |★[Stand2](https://www.amazon.co.jp/dp/B0B6DSD1RK/)|

### 道具類

|必須| 名前 | 備考 |参考商品|
|:-|:-|:-|:-|
|★|はんだごてセット|アマゾンの温度調整付きはんだごてセットがおすすめ。|[amazon](https://www.amazon.co.jp/dp/B0CM1WJB5X/)|
|★|プラスドライバー|M3ネジ締める用。||
|★|両面テープ|バッテリー固定用。無ければマスキングテープやビニテやガムテなどで代用可。||
||ピンセット|はんだ中のパーツ固定用。||
||マスキングテープ|はんだ中のパーツ固定用。||
||ニッパー|基板の分離用。||
||テスター|あると電源投入前に配線のショートをチェックできるので怖さが減ります。|[amazon](https://www.amazon.co.jp/dp/B07GJ891VR/)|

※参考商品は全てアフィリエイトの含まれない直リンクです

※参考商品はあくまで参考であり、全ての商品が検証済みではないことにご注意ください



　
## PCBの組み立て
### PCBの分離
- ニッパー等で赤丸で囲ったライナー部分をカットします。（素手でも折れると思います
![2025-03-05_14h26_51](https://github.com/user-attachments/assets/1c5e5bdd-da6b-4275-abbe-b84fb229dd7a)

### ホットスワップソケットのはんだづけ
- PCBの裏面に左右合計48箇所へホットスワップソケットを取り付けていきます。
> [!WARNING]
> - ソケットの向きに注意してください。ソケットのでっぱりとPCBのマークが一致するように。
> - はんだはたっぷり目で溶接してください。キースイッチ着脱中に脱落する原因になります。
  
![2025-03-05_14h10_34](https://github.com/user-attachments/assets/c9f43c88-1359-4b94-9ecb-af7309c57384)

### マイコンのはんだづけ
- PCBの表面にマイコンを仮付けします。マイコン付属のピンヘッダを装着し、PCBへ差し込んでマスキングテープ等で固定します。
![2025-03-05_14h11_43](https://github.com/user-attachments/assets/94695031-f662-4c99-bf90-5ff79c9273cb)
  
- PCB裏面からマイコンの背面パッド用の穴へはんだづけを行います（穴２つ、パッド４つ）。
> [!INFO]
> -はんだ作業後に左右のパッドがブリッジ（ショート）していないか、テスターを使って導通チェックすると安全です。（ショートを検知するとテスターからピー音が鳴ります
  
![2025-03-05_14h13_08](https://github.com/user-attachments/assets/5de233e1-3fa4-4c2b-bce4-cd5878d2cc05)
![2025-03-05_14h13_36](https://github.com/user-attachments/assets/21f33a4f-3479-4a94-b29c-a616f99a3ccd)
![2025-03-05_14h14_01](https://github.com/user-attachments/assets/6964582b-b896-4b80-a3d0-869d40fc8b76)


### ロータリーエンコーダーのはんだづけ
![2025-03-05_14h16_20](https://github.com/user-attachments/assets/3c965a6a-69f5-4381-8975-228ad65f82ce)


この時点で7割の作業が終わりです。お疲れ様でした。

### PCBへトッププレートとキースイッチの取り付け
![2025-03-05_14h19_45](https://github.com/user-attachments/assets/3bae6b06-6a4b-4cf7-9f9a-f9544f9a9fd6)


### FFCケーブルをPCBに取り付け
![2025-03-05_14h17_07](https://github.com/user-attachments/assets/285b2ccf-1c34-47ba-a621-3566103d62c3)

　
## D-Padモジュールの組み立て
### マイクロスイッチのはんだづけ
![2025-03-05_14h20_44](https://github.com/user-attachments/assets/ba3ddfe0-045e-4e32-8691-c76d01898ada)

### D-Padモジュールカバーの装着
![2025-03-05_14h21_26](https://github.com/user-attachments/assets/f91e2ae1-883b-4a3c-ba11-48e900c39661)
![2025-03-05_14h21_54](https://github.com/user-attachments/assets/e90cf2d4-0e0e-4339-8c59-39b13e86186a)
![2025-03-05_14h22_17](https://github.com/user-attachments/assets/357531fb-937c-40f5-8907-691a6c23b27e)


　
## キーボードの組み立て
### ケースの仮組み立て
ボトムプレートにマグネットとメタルプレートの取り付け
電源スイッチカバーの取り付け
![2025-03-05_14h23_55](https://github.com/user-attachments/assets/3601dbfd-2c2a-4ed9-8a4d-d465c9b14eba)

### トラックパッドとD-Pad取り付け
![2025-03-05_14h24_44](https://github.com/user-attachments/assets/5239e8d7-7912-4432-9762-cbaa0a2b26cd)
![2025-03-05_14h25_02](https://github.com/user-attachments/assets/f9bc118b-f268-4945-bdb2-46b4f3b19548)

　
## ファームウェアの書き込み＆動作確認(USB)

　
## バッテリー取り付け
![2025-03-05_14h25_35](https://github.com/user-attachments/assets/f810350d-b52e-44c9-b7ec-cd86a49ce65a)

#完成！！
