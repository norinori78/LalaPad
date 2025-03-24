# KeymapEditorの使い方

## GitHubアカウント作成する

- [Github](https://github.com/)のアカウントを作成します。
- ※自分用のファームウェアの管理及びファームウェアのビルドをする為に必要です
- ※アカウントの作り方の手順については割愛します
  


## LalaPadのファームウェアをフォークする（複製を作る的な奴

- [LalaPadのファームウェアリポジトリ](https://github.com/ShiniNet/zmk-config-LalaPad)にアクセス。
- リポジトリページの右上にあるForkボタンから「Create a new fork」する。
  
![2025-03-24_17h02_30](https://github.com/user-attachments/assets/83ba61de-95b6-4205-b846-3ea2d9425638)
  

- 何か色々聞かれるけどそのまま「Create fork」する。
  
![2025-03-24_17h10_07](https://github.com/user-attachments/assets/979d11b1-d21e-41f8-a837-41f475fc9acd)
  

- 自分のアカウント配下にLalaPadのファームウェアのフォークが作成されました。
  
![2025-03-24_17h12_36](https://github.com/user-attachments/assets/95b9bbb7-e9f4-43ff-bc37-6885977634f3)

## KeymapEditorを自分のGithubと連携する
- [KeymapEditor](https://nickcoutsos.github.io/keymap-editor/)のページを開く。
- 真ん中のGitHubのマークをクリックし、GitHubとの連携に進む。

![2025-03-24_17h06_56](https://github.com/user-attachments/assets/059d3a29-8bce-4793-abbb-66ab9a10deba)

  
- GitHubへのログイン画面が表示されるのでログインする。
- KeymapEditorを開いたブラウザと同じブラウザで既にGitHubログインしてある場合、そのまま確認画面へ飛びます。
- 確認画面では「次の画面ではOnly Select Repositoriesを選んでくださいね。」的な案内が表示されますので、そのまま「Add Repository」ボタン押下。
  
![2025-03-24_17h19_04](https://github.com/user-attachments/assets/0a926dd6-21b8-435c-ac6d-74a7d2e0afe4)

  
- GitHubにKeymapEditorをインストールする為の設定が開かれるので、「Only select repositories」を選択し、先ほどフォークしておいたLalaPadのファームウェアを指定します。
- Installボタンを押下します。

![2025-03-24_17h25_36](https://github.com/user-attachments/assets/64fc769a-2f12-4fe5-9b8f-eb5cbf03b517)

  
- キーボードのレイアウトが表示されていれば設定完了です！

![image](https://github.com/user-attachments/assets/6bda1ac1-2d46-4539-bbc1-281369356032)



## キーマップを変更し確定する

- 任意のレイヤーの任意のキーをクリックしてキーコード設定画面を開きます。
- [利用可能なキーコード](https://zmk.dev/docs/keymaps/list-of-keycodes)から任意のキーを選んで選択します。（検索窓にキーワード入力して探すと便利
  
![2025-03-24_17h41_06](https://github.com/user-attachments/assets/5795476b-f1cc-4fab-878e-158f3f38533c)
![2025-03-24_17h43_43](https://github.com/user-attachments/assets/a6b03ada-0493-40cc-9c71-ec8c58729990)

- KeymapEditor上でキーマップの変更を確認できたら「Save」ボタンを押下します。
- コミットコメントを求められるので、何のための変更かを任意の内容で入力し「Commit」します。
  
![2025-03-24_17h42_09](https://github.com/user-attachments/assets/2bad05f5-5deb-4b87-a553-dd2efc70e8b7)
![2025-03-24_17h46_04](https://github.com/user-attachments/assets/995ab9f1-b199-4024-8d96-eef91981f367)

- これでGithub側で自動ビルドが開始されます！
  


## 自動ビルドされたファームウェアをキーボードに投入する







