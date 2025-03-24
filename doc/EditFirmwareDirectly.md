# ファームウェアを直接カスタマイズする方法
<br/><br/>
## 大まかな流れ

1. ファームウェアのフォークを用意
2. WEBでソースコードを開く
3. 内容を編集してコミットする
4. ファームウェアが自動ビルドされるのでキーボードに書き込む
<br/><br/><br/>

## 準備：LalaPadのファームウェアのフォークを作成

- [KeymapEditorの使い方](https://github.com/ShiniNet/LalaPad/blob/main/doc/KeymapEdit.md)と同様。
- すでにフォークしたファームウェアを用意してある人はSKIP。
<br/><br/><br/>

## ファームウェアのソースコードをWEBで開く

- 自分のファームウェアのリポジトリのトップからConfigフォルダを開く
- ファイル一覧にある任意のソースコードを開く（今回はキーボードのプロパティを変更したいのでlalapad.confを開く）
  
![2025-03-24_21h12_32](https://github.com/user-attachments/assets/7ec78824-0b4a-4cdd-9f07-f4e544c9b403)
![2025-03-24_21h13_06](https://github.com/user-attachments/assets/1b781b95-2f3d-4d8f-b2cd-f56d9ede2c24)
<br/><br/><br/>

## ソースコードの内容を編集する

- コード内容の右上の鉛筆のマークをクリックして編集モードへ入る。
  
![2025-03-24_21h24_26](https://github.com/user-attachments/assets/742587f4-57f3-432f-bde3-306683798e92)
<br/><br/><br/>

- プロパティの内容を変更する（今回は「CONFIG_ZMK_IDLE_TIMEOUT」を変更し、アイドルモードへの移行を無効化する）
  
![2025-03-24_21h33_15](https://github.com/user-attachments/assets/92141fdc-06f5-493a-9170-7108f9542148)
<br/><br/><br/>

- ユーザーが弄る意味のありそうなプロパティ一覧
  
|プロパティ名|説明|
|:-|:-|
|CONFIG_ZMK_SLEEP|y:スリープ機能ON、n:スリープ機能OFF|
|CONFIG_ZMK_IDLE_TIMEOUT|キーボードが待機モードに入るまでの時間（MS単位）|
|CONFIG_ZMK_IDLE_SLEEP_TIMEOUT|キーボードがスリープモードに入るまでの時間（MS単位）|

その他のコンフィグ参考：[ZMK Doc - Configuration Overview](https://zmk.dev/docs/config)
<br/><br/><br/>

- 編集が完了したら右上のCommit Changesボタンを押下し、Commitコメントを入力したらコミットを確定する
  
![2025-03-24_21h15_46](https://github.com/user-attachments/assets/6ba33c41-26cb-47d7-b424-e75cc9f593a9)
<br/><br/><br/>

- これでファームウェアの自動ビルドが開始されます！

## 自動ビルドされたファームウェアをキーボードに書き込む

- [KeymapEditorの使い方](https://github.com/ShiniNet/LalaPad/blob/main/doc/KeymapEdit.md)と同様。
- なおKeymap以外のキーボードの構成を変更した場合、左右キーボード両方のファームウェアの更新が必要です。

