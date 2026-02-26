# GitHubへのアップロードとWeb公開の手順書

お疲れ様です！ローカル環境の準備が整いました。以下の手順で GitHub にアップロードし、Web公開を完了させてください。

## 1. 完了した準備内容
以下の作業を完了しました：
- **Web公開用のリネーム**: `Lumi-Vako_V1.0.html` を `index.html` に変更しました。
- **不要ファイルの除外**: GitHubに不要なファイル（ショートカット等）を除外する `.gitignore` を設定しました。
- **Gitの初期化**: フォルダをGitリポジトリとして初期化し、最初のコミット（スナップショット保存）を完了しました。
- **ドキュメントの整理**: `docs/github_upload_guide/` 内にこれまでの記録を保存しました。

## 2. GitHubでの操作（ユーザー様にお願いする作業）

### ステップ1：GitHubで新しいリポジトリを作成
1. [GitHub](https://github.com/) にログインします。
2. 画面右上の「+」アイコンから **New repository** を選択します。
3. **Repository name** に適切な名前（例：`lumi-vako`）を入力します。
4. **Public**（公開）を選択し、一番下の **Create repository** ボタンを押します。

### ステップ2：ファイルをアップロード
リポジトリ作成後の画面に表示される「quick setup」の手順に従います。

**一番簡単な方法：**
1. リポジトリのページにある **uploading an existing file** というリンクをクリックします。
2. フォルダ内のファイル一式（`.git` フォルダ**以外**すべて）をドラッグ＆ドロップします。
3. 下部の「Commit changes」ボタンを押します。

**コマンドラインで行う場合：**
（Gitに慣れている場合はこちらがスムーズです）
```bash
git remote add origin https://github.com/ユーザー名/リポジトリ名.git
git branch -M main
git push -u origin main
```

### ステップ3：GitHub Pages で Web 公開
1. 作成したリポジトリの **Settings**（設定）タブを開きます。
2. 左メニューの **Pages** をクリックします。
3. **Build and deployment** > **Source** が `Deploy from a branch` であることを確認します。
4. **Branch** で `main` (または `master`) を選び、フォルダを `/ (root)` に設定して **Save** を押します。
5. 数分待つと、上部に公開URL（`https://ユーザー名.github.io/リポジトリ名/`）が表示されます。

## 3. 公開後の確認
公開URLにアクセスし、正しく表示されるか確認してください。
`index.html` がトップページとして自動的に読み込まれます。
