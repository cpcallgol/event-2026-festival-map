# GitHub 投稿の仕方（はじめての人向け）

この説明書は、**GitHub を一度もさわったことがない人** でもできるように書いてあります。
上から順番に、書いてあるとおりにクリック・入力していけば大丈夫です。

- 🖱️ … クリックするところ
- ⌨️ … キーボードで入力するところ
- ✅ … うまくいったかの確認
- ⚠️ … まちがえやすいところ

---

## もくじ

| 番号 | やること | いつやる？ |
| --- | --- | --- |
| 0 | 全体の流れを知る | 最初に1回読む |
| 1 | GitHub のアカウントを作る | 最初の1回だけ |
| 2 | PC に Git と Python を入れる | PCごとに最初の1回だけ |
| 3 | GitHub に「箱（リポジトリ）」を作る | 最初の1回だけ |
| 4 | プロジェクトを箱につなぐ | 最初の1回だけ |
| 5 | はじめて送る（投稿する） | 最初の1回だけ |
| 6 | ホームページとして公開する（GitHub Pages） | 最初の1回だけ |
| 7 | いつもの更新のしかた | **毎回** |
| 8 | 別のPCで作業したいとき | 必要なときだけ |
| 9 | うまくいかないとき | こまったとき |

> いまの学校用の設定はすでに **1〜6 が終わっています**。
> ふだんは **「7. いつもの更新のしかた」だけ** やれば大丈夫です。

いまの設定:

| 項目 | 内容 |
| --- | --- |
| GitHub アカウント | `cpcallgol` |
| リポジトリ（箱） | `event-2026-festival-map` |
| リポジトリのページ | https://github.com/cpcallgol/event-2026-festival-map |
| 公開中の案内画面 | https://cpcallgol.github.io/event-2026-festival-map/ |

---

## 0. 全体の流れを知る

むずかしい言葉は、こう考えてください。

| ことば | たとえると |
| --- | --- |
| GitHub（ギットハブ） | インターネット上の **貸し倉庫** |
| アカウント | 倉庫を使うための **会員証** |
| リポジトリ | 倉庫の中の **1つの箱** |
| Git（ギット） | PC から倉庫へ荷物を運ぶ **トラック** |
| push（プッシュ） | トラックで荷物を **送ること** |
| GitHub Pages | 箱の中身を **ホームページとして貼り出してくれる係** |
| publish.bat | 荷物づくりから発送までを **全部やってくれるボタン** |

```
 [自分のPC]                                  [インターネット]

  編集画面で直す
      |
      | 「すべて保存」
      v
  publish.bat をダブルクリック  --- 送る --->  GitHub（倉庫の箱）
                                                  |
                                                  | 数分で自動的に貼り出す
                                                  v
                                       https://○○.github.io/○○/
                                                  |
                                                  v
                                       スマホ・家のPC・どこからでも見られる
```

---

## 1. GitHub のアカウントを作る（最初の1回だけ）

> すでにアカウント（`cpcallgol` など）を持っているなら、ここは飛ばしてください。

1. 🖱️ ブラウザ（Chrome や Edge）で **https://github.com** を開きます。
2. 🖱️ 右上の **「Sign up」**（サインアップ）を押します。
3. ⌨️ 画面の質問に答えていきます。
   - **Enter your email**：学校で使うメールアドレス
   - **Create a password**：パスワード（15文字以上、または8文字以上で数字と小文字を含む）
   - **Enter a username**：アカウント名（例：`cpcallgol`）
     ⚠️ この名前はホームページのアドレスになります。**あとから変えにくい** ので注意してください。
   - **Email preferences**：チェックは付けなくて大丈夫です
4. 🖱️ **「Continue」** を押して進みます。
5. 🖱️ 「ロボットではない確認」のパズルが出たら、指示どおりに解きます。
6. 📧 メールに届いた **8けたの数字（コード）** を ⌨️ 入力します。
7. 🖱️ 「How many team members…」などの質問は **「Just me」** や **「Skip personalization」** で大丈夫です。
8. 🖱️ プランを聞かれたら **「Free」（無料）** を選びます。

✅ 左上に GitHub のネコのマークが出て、自分のページが開けば完了です。

> 💡 パスワードとアカウント名は、紙やパスワード管理表に書いて保管しておきましょう。

---

## 2. PC に Git と Python を入れる（PCごとに最初の1回だけ）

### 2-1. 入っているか確認する

1. 🖱️ `koukasai_map_builder` フォルダーを開きます。
2. 🖱️ エクスプローラーの上の **アドレス欄**（フォルダーの場所が書いてあるところ）をクリックします。
3. ⌨️ `powershell` と入力して **Enter** を押します。
   青い画面（PowerShell）が開きます。
4. ⌨️ 次の2行を1行ずつ貼り付けて **Enter** を押します。

```powershell
git --version
py -3 --version
```

✅ `git version 2.○○` と `Python 3.○○` が出れば、両方入っています。**2-2 と 2-3 は飛ばしてください。**

⚠️ 「認識されません」と赤い文字が出たら、入っていません。次へ進みます。

### 2-2. Git を入れる

1. 🖱️ **https://git-scm.com/download/win** を開きます。
2. 🖱️ **「Click here to download」** を押してダウンロードします。
3. 🖱️ ダウンロードしたファイル（`Git-○○-64-bit.exe`）をダブルクリックします。
4. 🖱️ 質問はすべて **「Next」** を押して進み、最後に **「Install」** → **「Finish」** を押します。

### 2-3. Python を入れる

⚠️ 学校のPCでは、自分で入れられないことがあります。そのときは先生か管理者に
「Python 3 を入れてください」とお願いしてください。

1. 🖱️ **https://www.python.org/downloads/** を開きます。
2. 🖱️ 黄色い **「Download Python 3.○○」** を押します。
3. 🖱️ ダウンロードしたファイルをダブルクリックします。
4. ⚠️ 最初の画面の下にある **「Add python.exe to PATH」に必ずチェック** を入れます。
5. 🖱️ **「Install Now」** を押します。

### 2-4. 準備用のファイルを実行する

1. 🖱️ `koukasai_map_builder` フォルダーの **`setup.bat`** をダブルクリックします。
2. 黒い画面で文字が流れるので、終わるまで待ちます。

✅ 2-1 の確認をもう一度やって、両方のバージョンが出れば完了です。
（入れた直後は、PowerShell を一度閉じて開き直してください。）

---

## 3. GitHub に「箱（リポジトリ）」を作る（最初の1回だけ）

> いまの学校用の箱 `event-2026-festival-map` は **作成済み** です。新しく作り直すときだけやってください。

1. 🖱️ **https://github.com** を開き、使うアカウント（例：`cpcallgol`）でログインします。
   ⚠️ 右上の丸いアイコンを押して、**ログインしている名前が正しいか** 必ず確認してください。
2. 🖱️ 右上の **「＋」** を押して、**「New repository」** を押します。
3. ⌨️ 次のように入力・選択します。

| 項目 | 入れるもの |
| --- | --- |
| Owner | 自分のアカウント名（例：`cpcallgol`） |
| Repository name | 箱の名前（例：`event-2026-festival-map`）※英数字と `-` だけ |
| Description | 説明（なくてもよい。例：紅華祭の案内マップ） |
| 公開範囲 | **Public** を選ぶ |
| Add a README file | ⚠️ **チェックを入れない** |
| Add .gitignore | ⚠️ **None のまま** |
| Choose a license | ⚠️ **None のまま** |

4. 🖱️ 緑の **「Create repository」** を押します。

✅ 「Quick setup」と書かれた画面が出て、`https://github.com/アカウント名/箱の名前.git` というアドレスが表示されれば完了です。
このアドレスを次で使います。

> ⚠️ README などを付けて作ってしまうと、あとで送るときにエラーになります。
> そのときは箱を作り直すか、「9. うまくいかないとき」を見てください。

---

## 4. プロジェクトを箱につなぐ（最初の1回だけ）

> いまの PC は **cpcallgol の箱につないであります**。新しい箱にするときだけやってください。

1. 🖱️ `koukasai_map_builder` フォルダーを開きます。
2. 🖱️ アドレス欄をクリックして ⌨️ `powershell` と入力し、**Enter** を押します。
3. ⌨️ 次の3行を、**自分のアカウント名と箱の名前に書きかえてから**、1行ずつ貼り付けて **Enter** を押します。

```powershell
git remote set-url origin https://アカウント名@github.com/アカウント名/箱の名前.git
git config user.name "アカウント名"
git config user.email "アカウント名@users.noreply.github.com"
```

いまの学校用の場合は、こうなります。

```powershell
git remote set-url origin https://cpcallgol@github.com/cpcallgol/event-2026-festival-map.git
git config user.name "cpcallgol"
git config user.email "cpcallgol@users.noreply.github.com"
```

> 💡 アドレスの `https://` のあとに `アカウント名@` を入れるのがポイントです。
> こうすると、PC に別のアカウントのログイン情報が残っていても、正しいアカウントで送れます。

4. ⌨️ つながったか確認します。

```powershell
git remote -v
```

✅ 次のように、自分の箱のアドレスが2行出れば完了です。

```
origin  https://cpcallgol@github.com/cpcallgol/event-2026-festival-map.git (fetch)
origin  https://cpcallgol@github.com/cpcallgol/event-2026-festival-map.git (push)
```

⚠️ `error: No such remote 'origin'` と出たときは、`set-url` のかわりに次を使います。

```powershell
git remote add origin https://アカウント名@github.com/アカウント名/箱の名前.git
```

---

## 5. はじめて送る（最初の1回だけ）

1. ⌨️ 4 と同じ PowerShell で、次を貼り付けて **Enter** を押します。

```powershell
git push -u origin main
```

2. 🖱️ **GitHub のログイン画面** が出ます。⚠️ **絶対に閉じないでください。**
   - 🖱️ **「Sign in with your browser」** を押します。
   - ブラウザが開くので、🖱️ **正しいアカウント（例：cpcallgol）** でログインします。
   - 🖱️ **「Authorize git-ecosystem」**（許可する）を押します。
   - 「Authentication Succeeded」と出たら、ブラウザは閉じて大丈夫です。

⚠️ ブラウザで別のアカウントにログインしたままだと、そちらで許可してしまいます。
先に github.com の右上で、**正しいアカウントに切り替えてから** 押してください。

✅ PowerShell に次のような文字が出たら成功です。

```
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.
```

> 💡 PowerShell では、成功していても赤い文字が混ざって表示されることがあります。
> **`[new branch]` や `main -> main` があれば成功** です。

✅ ブラウザで自分の箱のページ（例：https://github.com/cpcallgol/event-2026-festival-map ）を開き直すと、
`docs` `static` `templates` などのフォルダーが並んでいます。

⚠️ `fatal: User cancelled dialog.` と出たら、ログイン画面を閉じてしまっています。もう一度 1 からやってください。

---

## 6. ホームページとして公開する（GitHub Pages・最初の1回だけ）

1. 🖱️ ブラウザで自分の箱のページを開きます。
2. 🖱️ 上のメニューの右のほうにある **「⚙ Settings」**（設定）を押します。
   ⚠️ Settings が見えないときは、ログインしているアカウントがちがいます。
3. 🖱️ 左のメニューを下にスクロールして、**「Pages」** を押します。
4. 「Build and deployment」のところを、次のようにします。

| 項目 | 選ぶもの |
| --- | --- |
| Source | 🖱️ **Deploy from a branch** |
| Branch（左） | 🖱️ **main** |
| フォルダー（右） | 🖱️ **/docs** |

5. 🖱️ **「Save」** を押します。
6. ⏳ **5分くらい** 待ってから、🖱️ ページを再読み込み（**F5**）します。

✅ 上のほうに **「Your site is live at https://○○.github.io/○○/」** と出れば公開完了です。
その「Visit site」を押すと、案内画面が開きます。

⚠️ Branch に **None しか出ない** ときは、まだ何も送れていません。「5. はじめて送る」をやり直してください。

---

## 7. いつもの更新のしかた（毎回これだけ）

### ステップ1：編集画面で直して保存する

1. 🖱️ `start_editor.bat` をダブルクリックします。編集画面がブラウザで開きます。
2. 🖱️ ピンや企画を直します。
3. 🖱️ 右上の緑の **「すべて保存」** を押します。

✅ 右上が **「保存済み」** になり、下に「保存しました」と出れば OK です。

⚠️ 「すべて保存」を押し忘れると、何も送られません。

### ステップ2：publish.bat をダブルクリックする

1. 🖱️ `koukasai_map_builder` フォルダーの **`publish.bat`** をダブルクリックします。
2. 黒い画面で文字が流れるので、待ちます。

✅ 最後にこう出たら成功です。

```
公開しました。インターネット上の案内画面には数分で反映されます。
続行するには何かキーを押してください . . .
```

3. ⌨️ 何かキー（Enter など）を押して、黒い画面を閉じます。

> 💡 途中でログイン画面が出たら、「5. はじめて送る」の 2 と同じようにログインしてください。

### ステップ3：待ってから確認する

1. ⏳ **5分くらい** 待ちます。
2. 🖱️ 公開中の案内画面（例：https://cpcallgol.github.io/event-2026-festival-map/ ）を開きます。
3. 古いままなら ⌨️ **Ctrl を押しながら F5** を押して読み込み直します。

> 💡 進み具合は、箱のページの **「Actions」** タブで見られます。
> 🟡 黄色の丸 = 作業中、✅ 緑のチェック = 公開完了、❌ 赤のバツ = 失敗 です。

---

## 8. 別のPCで作業したいとき

### はじめての PC（最初の1回だけ）

1. 「2. PC に Git と Python を入れる」をやります。
2. 🖱️ プロジェクトを置きたいフォルダーを開き、アドレス欄に ⌨️ `powershell` と入力して **Enter** を押します。
3. ⌨️ 次の3行を1行ずつ貼り付けて **Enter** を押します。

```powershell
git clone https://cpcallgol@github.com/cpcallgol/event-2026-festival-map.git koukasai_map_builder
git -C koukasai_map_builder config user.name "cpcallgol"
git -C koukasai_map_builder config user.email "cpcallgol@users.noreply.github.com"
```

4. 🖱️ できた `koukasai_map_builder` フォルダーの **`setup.bat`** をダブルクリックします。

> 💡 GitHub には、バックアップ（`data\backups`）や元の画像（`data\image_originals`）は送っていません。
> そのため、新しい PC にはこれらは入っていません。案内画面の表示には影響ありません。

### 編集を始める前に、毎回やること

ほかの PC で更新したあとは、**編集する前に必ず最新を取り込みます。**

1. 🖱️ `koukasai_map_builder` フォルダーでアドレス欄に ⌨️ `powershell` と入力して **Enter** を押します。
2. ⌨️ 次を貼り付けて **Enter** を押します。

```powershell
git pull
```

✅ `Already up to date.` か、ファイル名がいくつか出れば完了です。

⚠️ **2台の PC で同時に編集しないでください。** あとから送ったほうがぶつかってエラーになります。

---

## 9. うまくいかないとき

黒い画面や PowerShell に出た文字を見て、下から同じものを探してください。

### `fatal: User cancelled dialog.`

- ログイン画面を閉じてしまっています。
- もう一度送り直し、ログイン画面が出たら **閉じずに** ログインしてください。

### `Permission to ○○ denied to △△` / `403`

- **ちがうアカウント（△△）** で送ろうとしています。
- 次の順番で直します。
  1. 🖱️ Windows のスタートボタンを押し、⌨️ `資格情報マネージャー` と入力して開きます。
  2. 🖱️ **「Windows 資格情報」** を押します。
  3. 🖱️ `git:https://github.com` の行を開いて、**「削除」** を押します。
  4. もう一度送り、**正しいアカウント** でログインします。

### `! [rejected] main -> main (fetch first)`

- GitHub の箱のほうに、PC にない変更があります（別の PC で更新した、など）。
- ⌨️ `git pull` を実行してから、もう一度 `publish.bat` を実行してください。

### `Updates were rejected because the remote contains work that you do not have`（はじめて送るとき）

- 箱を作るときに README などを付けてしまっています。
- いちばん簡単なのは、**箱を削除して作り直す** ことです（「3. 箱を作る」で README にチェックを入れない）。
  - 削除のしかた：🖱️ 箱の **Settings** → いちばん下の **「Delete this repository」**

### `変更はありません。`

- 前回送った内容と同じです。
- 編集画面で **「すべて保存」を押したか** 確認してください。

### `[ERROR] Python 3 が見つかりません。`

- 「2-3. Python を入れる」をやってください。

### `[ERROR] Git が見つかりません。`

- 「2-2. Git を入れる」をやってください。

### `PermissionError: [WinError 32] … 別のプロセスが使用中です`

- `docs` フォルダーを、ほかのアプリ（エクスプローラー、エディター、確認用のサーバーなど）が開いています。
- 開いているウィンドウを閉じてから、もう一度 `publish.bat` を実行してください。

### 公開ページが「案内情報を読み込めませんでした」になる

- 数分待ってから ⌨️ **Ctrl + F5** で読み込み直してください。
- それでも直らないときは、`start_main.bat` で自分の PC の案内画面（http://127.0.0.1:5000/ ）が正しく出るか確認してください。

### 公開ページが古いまま

- GitHub は貼り出しに **数分〜10分** かかります。待ってから ⌨️ **Ctrl + F5** を押してください。
- 箱のページの **「Actions」** タブで、緑のチェックが付いているか確認してください。

### Pages の Branch で None しか選べない

- 箱がまだ空っぽです。「5. はじめて送る」をやって、成功の表示が出るか確認してください。

---

## やってはいけないこと

- ⚠️ **`docs` フォルダーの中を手で直さない。** `publish.bat` が毎回作り直すので、手で直しても消えます。
- ⚠️ **個人情報を載せない。** 公開ページは世界中のだれでも見られます。名前・電話番号・顔写真などは載せないでください。
- ⚠️ **リポジトリを Private（非公開）にしたり、削除したりしない。** 公開ページが見られなくなります。
- ⚠️ **パスワードやトークンを人に教えない・ファイルに書かない。**
- ⚠️ **2台の PC で同時に編集しない。**

> GitHub に送らないもの（自動で除外しています）:
> `data\backups`（バックアップ）、`data\image_originals`（元の画像）、`server_address.txt`（学校内のアドレス）
