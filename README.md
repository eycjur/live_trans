# Live Trans

英語の音声をリアルタイムで文字起こし・翻訳するシングルページアプリです。

## 機能

- マイクから英語を認識し、発言ごとにテキスト化
- 日本語・中国語・韓国語・フランス語など8言語へリアルタイム翻訳
- Chrome Translation API による翻訳（オフライン対応）
- 全文字起こしのクリップボードコピー

## 使用技術

| 機能 | 技術 |
|------|------|
| 文字起こし | [Web Speech API](https://developer.mozilla.org/ja/docs/Web/API/Web_Speech_API)（`SpeechRecognition`、英語認識） |
| 翻訳 | [Chrome Translation API](https://developer.chrome.com/docs/ai/translator-api)（`window.translation`） |

## 開発環境

```bash
npx serve .
```

ブラウザで `http://localhost:3000` を開き、「録音開始」を押して英語で話してください。

> `file://` で直接開くと Web Speech API がブロックされるため、ローカルサーバー経由でのアクセスが必要です。

## 動作環境

各 API に対応したブラウザが必要です。未対応の場合、画面上にエラーが表示され該当機能は利用できません。

| 機能 | 対応ブラウザ |
|------|------------|
| 文字起こし（Web Speech API） | Chrome、Edge |
| 翻訳（Chrome Translation API） | デスクトップ版 Chrome 131 以降（要フラグ有効化） |

> **モバイル非対応：** Chrome Translation API はデスクトップ専用のため、モバイルでは翻訳機能が利用できません。

### Chrome Translation API の有効化

`chrome://flags` で以下を **Enabled** に設定してください。

- `Translator API`
- `Translator API for Localhost`（ローカル開発時）

## ファイル構成

```
index.html   # アプリ本体（HTML + CSS + JS のシングルファイル）
```
