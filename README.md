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

- Chrome または Edge（Web Speech API 対応ブラウザ）

## ファイル構成

```
index.html   # アプリ本体（HTML + CSS + JS のシングルファイル）
```
