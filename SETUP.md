# 戦国五陣 Online — 2台対戦の準備

## GitHub Pages
URL: https://onigiript.github.io/sengoku-gojin/

## Firebase 設定
1. https://console.firebase.google.com/ でプロジェクトを作成
2. プロジェクトにWebアプリを追加（Firebase Hosting は不要）
3. Authentication → Sign-in method → 匿名を有効にする
4. Realtime Database を作成し、**Rules** に database.rules.json の内容を貼って Publish（公開）
5. Project settings → Your apps → SDK setup and configuration → Config に出る `firebaseConfig` の値を `firebase-config.js` の対応する項目に入力。**databaseURL は必須**。
6. GitHub Pagesでゲームを開き、1台目で部屋作成、2台目で参加して動作確認

## 注意
このアプリは家族内テスト向けの試作版です。ゲーム状態をデータベース内に保存するため、対戦相手にはカードの秘密情報を技術的に閲覧できる可能性があります。ルールも完成版ではなく、今後サーバー側検証、部屋の権限制限、特殊能力、制圧判定の調整が必要です。データベースルールは無認証で全公開する設定（true/true）にしないでください。
