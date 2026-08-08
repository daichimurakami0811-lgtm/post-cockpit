# Post Cockpit v20 — Deployment Package

## Files

- `index.html` — Post Cockpit本体
- `post-cockpit-personas.json` — 外部ペルソナ定義

## Local test

HTTPサーバー経由で起動してください。

### Python
```bash
python -m http.server 8000
```

その後:
http://localhost:8000/

### Node.js
```bash
npx serve .
```

## Deployment

静的ホスティングにこのフォルダの2ファイルをアップロードします。

推奨:
- Cloudflare Pages
- Netlify
- Vercel
- GitHub Pages

## API keys

APIキーはコードに埋め込まないでください。
Post CockpitのAPI設定画面から入力してください。

## Webhook

GAS / MakeなどのWebhook URLを設定画面に登録します。

ブラウザから外部Webhookへ直接POSTする場合、送信先側でCORSを許可する必要があります。

## Important

`post-cockpit-personas.json` を変更した場合、同じファイル名のまま公開先のファイルを更新してください。
