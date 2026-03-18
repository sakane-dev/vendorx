[ README.md (日本語) ]

# Island.io GTM Strategy - Executive Briefing
## 多言語対応しました
2026.03.18
i18nの実装により、8か国語に対応しました（日本語、英語、中国語、韓国語、フランス語、ロシア語、ドイツ語、イタリア語）。

## プロジェクトの概要
本プロジェクトは、Island.ioの日本市場進出におけるGo-To-Market（GTM）戦略を経営層へ提示するための、シングルページアプリケーション（SPA）形式のプレゼンテーションプロトタイプです。

単なる情報の羅列ではなく、認知科学および行動経済学（プロスペクト理論、メンタルアカウンティング、ハロー効果など）の知見を応用した「SlideOps標準デザイン仕様」に基づいて設計されています。シネマティック・グラスモーフィズムを採用したUIと、多言語対応のシームレスなトランジションにより、エグゼクティブ層の意思決定を最適化する視覚的アーティファクトとして機能します。

## 主要な特徴
* 認知科学に基づくUI/UX設計: 視覚的権威性を高めるタイポグラフィと、コンテキストに連動した背景画像の動的マッピングにより、読み手の流暢性を向上させています。
* 対話型AIアシスタントの統合: Google Gemini APIをレバレッジしたRAG（Retrieval-Augmented Generation）風のチャットボットを内包し、スライドの文脈に基づいた質疑応答をリアルタイムで提供します。
* セキュアなアーキテクチャ: クレデンシャル（APIキー）のハードコードやキャッシュを排除し、セッション実行時のみメモリ上で処理するセキュアな設計を採用しています。
* 多言語シームレス切り替え: 再読み込みを伴わないインメモリのデータバインディングにより、日本語と英語のUIを瞬時に切り替えることが可能です。
* 動的プレゼンテーション制御: 時間経過によるオートスクロール機構と、マウスホイールによる水平スクロール変換ロジックを実装しています。

## 技術スタック
* フロントエンド: HTML5, CSS3 (CSS Variables, CSS Grid/Flexbox), Vanilla JavaScript
* AI統合: Google Gemini API (gemini-2.5-flash)
* アセット配信: Unsplash Image API (Global CDN)
* ホスティング: GitHub Pages

## 使用方法
1. GitHub Pagesの公開URLにアクセスします。
2. スライドは8秒間隔で自動的に横スクロールします。マウスホバーで自動スクロールは一時停止し、マウスホイールやキーボードの左右矢印キーで手動操作が可能です。
3. 画面右上の言語切り替えボタンで、日本語と英語の表示を切り替えます。
4. 画面右下の「AI」ボタンをクリックすると、戦略アシスタントのチャットインターフェースが起動します。
5. チャットボットを使用する場合は、入力フィールドに有効なGemini APIキーを入力した上で、資料に関する質問を送信してください。

## セキュリティに関する留意事項
本アプリケーションは完全なクライアントサイド実装です。入力されたGemini APIキーは、通信の瞬間のみリクエストヘッダとして組み立てられ、ブラウザのローカルストレージやCookie等には一切保存されません。ブラウザのタブを閉じるかリロードした段階で、キー情報は揮発します。

## 著作権および免責事項
本プレゼンテーションに記載されているGTM戦略、ROIの数値、およびコスト削減モデルは、分析に基づく仮説およびシミュレーションであり、実際の数値を保証するものではありません。
作成者: 坂根康之 (yasuyuki@sakane.dev)

---

[ README.md (English) ]

# Island.io GTM Strategy - Executive Briefing

## Project Overview
This project is a Single Page Application (SPA) presentation prototype designed to articulate the Go-To-Market (GTM) strategy for Island.io's entry into the Japanese market, specifically tailored for executive leadership.

Moving beyond simple information display, the architecture is grounded in the "SlideOps Standard Design Specifications," applying principles from cognitive science and behavioral economics such as Prospect Theory, Mental Accounting, and the Halo Effect. Utilizing a cinematic glassmorphism UI and seamless multilingual transitions, it serves as a visual artifact optimized for executive decision-making.

## Key Features
* UI/UX Design Based on Cognitive Science: Enhances processing fluency through authoritative typography and dynamic mapping of context-aware background images.
* Integrated Conversational AI Assistant: Embeds a chatbot powered by the Google Gemini API, functioning similarly to Retrieval-Augmented Generation (RAG), to provide real-time Q&A based on the presentation's context.
* Secure Architecture: Eliminates hardcoding or caching of credentials. The API key is securely processed in-memory only during the active session.
* Seamless Multilingual Switching: Achieves instantaneous switching between Japanese and English UIs without page reloads, utilizing in-memory data binding.
* Dynamic Presentation Control: Implements an auto-scroll mechanism based on time intervals, alongside logic that converts vertical mouse wheel input into horizontal scrolling.

## Technology Stack
* Front-end: HTML5, CSS3 (CSS Variables, CSS Grid/Flexbox), Vanilla JavaScript
* AI Integration: Google Gemini API (gemini-2.5-flash)
* Asset Delivery: Unsplash Image API (Global CDN)
* Hosting: GitHub Pages

## Usage
1. Access the published GitHub Pages URL.
2. Slides will automatically scroll horizontally every 8 seconds. Hovering the mouse will pause the auto-scroll, allowing for manual navigation using the mouse wheel or keyboard arrow keys.
3. Use the language toggle button in the top right corner to switch between Japanese and English.
4. Click the "AI" button in the bottom right corner to launch the strategic assistant chat interface.
5. To use the chatbot, enter a valid Gemini API key in the designated field and submit your questions regarding the presentation materials.

## Security Considerations
This application is implemented entirely on the client side. The entered Gemini API key is assembled into the request header only at the moment of communication and is never stored in the browser's local storage or cookies. The key information is volatile and is cleared when the browser tab is closed or reloaded.

## Copyright and Disclaimer
The GTM strategy, ROI figures, and cost reduction models presented in this document are hypotheses and simulations based on analysis and do not guarantee actual financial outcomes.
Author: Yasuyuki Sakane (yasuyuki@sakane.dev)

---

ご不明な点や追加の要件がございましたら、お知らせください。
