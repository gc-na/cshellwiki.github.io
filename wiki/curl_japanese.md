# [Linux] Bash curl の使い方: HTTPリクエストを送信する

## Overview
`curl` コマンドは、URLを介してデータを転送するためのツールです。主にHTTP、HTTPS、FTPなどのプロトコルを使用して、リモートサーバーとデータをやり取りする際に利用されます。

## Usage
基本的な構文は以下の通りです。

```
curl [options] [arguments]
```

## Common Options
- `-X` : 使用するHTTPメソッドを指定します（例: GET, POST）。
- `-d` : POSTリクエストで送信するデータを指定します。
- `-H` : リクエストヘッダーを追加します。
- `-o` : 出力ファイル名を指定します。
- `-I` : ヘッダーのみを取得します。

## Common Examples
1. **基本的なGETリクエスト**
   ```bash
   curl http://example.com
   ```

2. **POSTリクエストでデータを送信**
   ```bash
   curl -X POST -d "name=John&age=30" http://example.com/api
   ```

3. **カスタムヘッダーを追加**
   ```bash
   curl -H "Authorization: Bearer token" http://example.com/protected
   ```

4. **レスポンスをファイルに保存**
   ```bash
   curl -o output.html http://example.com
   ```

5. **ヘッダーのみを取得**
   ```bash
   curl -I http://example.com
   ```

## Tips
- `-s` オプションを使用すると、進行状況やエラーメッセージを表示せずに実行できます。
- `-L` オプションを使うと、リダイレクトを自動的に追跡します。
- 複雑なAPIリクエストを行う際は、JSONデータを送信するために `-H "Content-Type: application/json"` を使用することをお勧めします。