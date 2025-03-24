# KeymapEditorの使い方

## 大まかな流れ
1. GitHubアカウント作る
2. LalaPadのファームをフォーク（複製）する
3. KeymapEditorで↑を読み込み好き放題キーマップ弄る
4. 自動ビルドされたファームウェアをダウンロードしてキーボードへ書き込む
   

　　※以降、キーマップの変更は3と4だけやればOK
<br/><br/><br/>
## GitHubアカウント作成する

- [Github](https://github.com/)のアカウントを作成します。
- ※自分用のファームウェアの管理及びファームウェアのビルドをする為に必要です
- ※アカウントの作り方の手順については割愛します
  
<br/><br/><br/>

## LalaPadのファームウェアをフォークする（複製を作る的な奴

- [LalaPadのファームウェアリポジトリ](https://github.com/ShiniNet/zmk-config-LalaPad)にアクセス。
- リポジトリページの右上にあるForkボタンから「Create a new fork」する。
  
![2025-03-24_17h02_30](https://github.com/user-attachments/assets/83ba61de-95b6-4205-b846-3ea2d9425638)
  <br/><br/><br/>

- 何か色々聞かれるけどそのまま「Create fork」する。
  
![2025-03-24_17h10_07](https://github.com/user-attachments/assets/979d11b1-d21e-41f8-a837-41f475fc9acd)
  <br/><br/><br/>

- 自分のアカウント配下にLalaPadのファームウェアのフォークが作成されました。
- Actionのタブへ遷移し、GitHubAcitonを有効にしておきます。
- 「I understand my workflows, go ahead and enable them」ボタンを押下します。
  
![2025-03-24_17h55_38](https://github.com/user-attachments/assets/1424bfe5-233d-450f-964b-d3a258d23b48)
![2025-03-24_17h55_47](https://github.com/user-attachments/assets/277b82c6-e40f-44be-a147-d23d4e13102e)
　<br/><br/><br/>

## KeymapEditorを自分のGithubと連携する
- [KeymapEditor](https://nickcoutsos.github.io/keymap-editor/)のページを開く。
- 真ん中のGitHubのマークをクリックし、GitHubとの連携に進む。

![2025-03-24_17h06_56](https://github.com/user-attachments/assets/059d3a29-8bce-4793-abbb-66ab9a10deba)
　<br/><br/><br/>
  
- GitHubへのログイン画面が表示されるのでログインする。
- KeymapEditorを開いたブラウザと同じブラウザで既にGitHubログインしてある場合、そのまま確認画面へ飛びます。
- 確認画面では「次の画面ではOnly Select Repositoriesを選んでくださいね。」的な案内が表示されますので、そのまま「Add Repository」ボタン押下。
  
![2025-03-24_17h19_04](https://github.com/user-attachments/assets/0a926dd6-21b8-435c-ac6d-74a7d2e0afe4)
　<br/><br/><br/>
  
- GitHubにKeymapEditorをインストールする為の設定が開かれるので、「Only select repositories」を選択し、先ほどフォークしておいたLalaPadのファームウェアを指定します。
- Installボタンを押下します。

![2025-03-24_17h25_36](https://github.com/user-attachments/assets/64fc769a-2f12-4fe5-9b8f-eb5cbf03b517)
<br/><br/><br/>
  
- KeymapEditorの画面に自動的に戻り、キーボードのレイアウトが表示されていれば設定完了です！

![image](https://github.com/user-attachments/assets/6bda1ac1-2d46-4539-bbc1-281369356032)
<br/><br/><br/>


## キーマップを変更し確定する

- 任意のレイヤーの任意のキーをクリックしてキーコード設定画面を開きます。
- [利用可能なキーコード](https://zmk.dev/docs/keymaps/list-of-keycodes)から任意のキーを選んで選択します。（検索窓にキーワード入力して探すと便利
  
![2025-03-24_17h41_06](https://github.com/user-attachments/assets/5795476b-f1cc-4fab-878e-158f3f38533c)
![2025-03-24_17h43_43](https://github.com/user-attachments/assets/a6b03ada-0493-40cc-9c71-ec8c58729990)
<br/><br/><br/>

- KeymapEditor上でキーマップの変更を確認できたら「Save」ボタンを押下します。
- コミットコメントを求められるので、何のための変更かを任意の内容で入力し「Commit」します。
  
![2025-03-24_17h42_09](https://github.com/user-attachments/assets/2bad05f5-5deb-4b87-a553-dd2efc70e8b7)
![2025-03-24_17h46_04](https://github.com/user-attachments/assets/995ab9f1-b199-4024-8d96-eef91981f367)
<br/><br/>
- これでGithub側で自動ビルドが開始されます！
  
<br/><br/><br/>

## 自動ビルドされたファームウェアをキーボードに投入する

- 自分のGitHubのAcitonタブを開きます。
- ビルド一覧が表示されますので、最新のビルドを選択します。
- ※KeymapEditor上でSaveを押下してからビルド完了まで大体2~3分かかります。
  
![2025-03-24_18h03_00](https://github.com/user-attachments/assets/3644a8e5-c4db-4d6d-851c-e8a56f5e22de)
<br/><br/><br/>

- ビルドが正常に終了していればグリーンのアイコンが表示され、ファームウェアがダウンロード可能になっています。
- 画面下部のダウンロードボタンを押下してファイル（ZIP形式）をダウンロードしてください。

![2025-03-24_18h05_50](https://github.com/user-attachments/assets/56f14e2f-5b2c-4f2e-b002-ae6869b6ee0f)
<br/><br/><br/>

- firmware.zipの中身を開くとUF2ファイルが格納されていますので、ビルドガイドと同様の手順でそれぞれを左右のキーボードへ書き込みます。
  
![2025-03-24_18h08_08](https://github.com/user-attachments/assets/1f467a8d-5bf4-4919-bcfb-2fa0c616a931)
<br/><br/><br/>

以上！
