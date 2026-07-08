# [English] SlideOps Framework Specification

SlideOps is a next-generation presentation framework independently developed by `sakane.dev`. It is designed from an interdisciplinary perspective that integrates insights from software engineering, cognitive science, and behavioral economics to fundamentally redefine the process of creating and delivering business presentations.
Its greatest uniqueness lies in the fact that "the system automatically generates compelling slides optimized for human cognitive biases, without the user ever needing to consciously consider psychology or design." The author focuses purely on the "logic to be conveyed (Markdown)," while all the remaining "psychological and visual transformations required to communicate effectively" are autonomously executed by CI/CD pipelines and AI agents.

---

## 🌟 The Uniqueness and Interdisciplinary Perspective of SlideOps

Traditional presentations (e.g., PowerPoint) tightly couple content (data) with design (expression), which easily generates person-dependent design debt and makes information reuse difficult. SlideOps breaks through these limitations via the following interdisciplinary approaches:

*   **"Unconscious" Automated Implementation of Cognitive Science**
    The user simply inputs bulleted text, and the integrated LLM (Language Model) reads the underlying context. It autonomously applies behavioral economics frameworks—such as Prospect Theory (stimulating loss aversion), the Anchoring Effect, and breaking the Status Quo Bias—to determine the optimal layout structure (e.g., conversion to comparison tables or highlighting key metrics).
*   **Continuous Application of a Powerful "Halo Effect"**
    Using the 2026 Silicon Valley standard (True Dark, Spatial Neumorphism) and typography that minimizes cognitive load, the design system is centrally controlled via JSON definitions. This eliminates person-dependent layout collapses and imparts an unconscious sense of authority ("advanced and reliable"—the Halo Effect) to the audience, regardless of who created the slides.
*   **Liquefaction and Multi-use of Content (Docs-as-Code)**
    Information is not locked into a specific binary file but treated as pure text data. Once the logical structure is written, it dynamically and flexibly transforms (liquefies) not only into dynamic HTML slides but simultaneously into whitepapers (PDFs) or JSON-APIs for web marketing.
*   **Data-Driven Autonomous Evolution (Telemetry & Feedback)**
    Deployed slides collect behavioral logs, such as audience dwell time and micro-interactions (clicks, etc.). If the cognitive load of a slide is deemed too high (e.g., dwell time exceeds a threshold), the system features an evolutionary loop where the AI autonomously simplifies the expression during the next pipeline execution.

---

## 🏛️ Core Architecture

SlideOps is built on three layers, based on the Separation of Concerns.

### Layer 1: Source Layer (Single Source of Truth / Data Definition)

The only layer edited directly by humans. No visual or psychological specifications are made here.

*   **`content.md` (Markdown):** The pure text information and logical structure (H1, lists, etc.) of the presentation.
*   **`context.yaml` (YAML):** Contextual metadata such as the target audience (e.g., Manufacturing CFO), objective (breaking sunk cost), and expected tone.
*   **`design_system.json` (JSON):** The brand's visual rule set optimized via cognitive science, including color schemes, Variable Fonts stacks, and spacing definitions based on the Fibonacci sequence.

### Layer 2: Pipeline Layer (AI Orchestration and Generation)

A "cognition and expression transformation" pipeline triggered by Git Push.

*   **AI Architect Agent:** An LLM analyzes `content.md` and `context.yaml` to generate structured data (`structure.json`) infused with optimal psychological approaches. Simultaneously, it executes translations (i18n) considering the cultural background of the target language (en, zh-TW, etc.).
*   **Generator Engine:** Using tools like Astro and Tailwind CSS, it dynamically combines the generated structural data and `design_system.json` to render HTML/CSS. Animations that create high Processing Fluency are also applied here.
*   **QA Agent:** Runs headless browser tests via Playwright to detect and self-heal defects such as text overflow and accessibility (contrast ratio) issues.

### Layer 3: Delivery & Telemetry Layer (Deployment and Dynamic Evaluation)

The layer that deploys the generated output and collects feedback.

*   **Multi-Export:** Deploys HTML to edge networks like Netlify while simultaneously pushing data to API endpoints for marketing tools.
*   **Telemetry (Behavioral Logs):** When dwell time per slide exceeds a threshold (suggesting increased cognitive load) or interaction is low, this data is fed back to the orchestrator to dynamically adjust prompts.

---

## 🔄 Operational Workflow

By adopting SlideOps, the business workflow for creating presentations is refined to the extreme.

1.  **Drafting:** The creator writes only the logic of the message ("what to convey") in Markdown, without worrying at all about design or appearance.
2.  **Committing:** The completed Markdown and context (YAML) are committed to a Git repository. **(Manual human intervention completely ends here.)**
3.  **Automated Structuring:** An orchestrator (e.g., n8n) triggers in the background, where AI transforms the data into a psychologically and visually optimized structure, including multilingualization.
4.  **Building & Testing:** A static site generator builds the latest HTML design and passes automated QA tests.
5.  **Deployment:** Within minutes, a presentation URL engineered with an interdisciplinary approach is issued, enabling immediate presentation and sharing.

---

## 🎨 Visual Language and Cognitive Palette (SlideOps v1.0 Design)

The visual language built into the framework fuses the 2026 Silicon Valley standard (OLED optimization, Spatial Neumorphism) with cognitive psychology.

*   **True Dark Background (`#030712`):** A pitch-black background that prevents eye fatigue and makes foreground information float in space.
*   **Emotional Manipulation via Signal Colors:**
    *   Cognitive Indigo (`#6366F1`), symbolizing trust and authority.
    *   Thermal Rose (`#F43F5E`), deeply stimulating loss aversion while maintaining sophistication.
*   **Typography:** Settings like Tabular Numbers to enhance the persuasive power of quantitative data, and dynamic bindings of universal design fonts to prevent misreading even from a distance.

---

## 🚀 Conclusion: The Paradigm Shift Brought by SlideOps

SlideOps is not merely an "automated slide generation tool."

It reduces wasted time spent tweaking presentation designs to "zero," allowing human resources to focus exclusively on essential intellectual production: "strategy construction." And, as the system automatically supplements best practices from cognitive science and behavioral economics, **anyone in the organization can highly reproducibly generate presentations with world-class persuasive power.**

SlideOps is the practice of true Platform Engineering, fundamentally transforming the speed of corporate decision-making and the quality of communication.

---

# [Japanese] SlideOps Framework 仕様書

SlideOpsとは、sakane.devが独自開発した新世代のプレゼンテーション作成フレームワークです。ソフトウェア工学、認知科学、行動経済学の知見を統合し、ビジネスプレゼンテーションの作成・運用プロセスを根本から再定義する学際的視座から設計、開発されています。
最大の特異性は、「ユーザーが心理学やデザインを一切意識することなく、システムが自動的に人間の認知バイアスに最適化された説得力のあるスライドを生成する」点にあります。書き手は純粋な「伝えるべき論理（Markdown）」にのみ集中し、残りの「伝わるための心理的・視覚的変換」はすべてCI/CDパイプラインとAIエージェントが自律的に実行します。

---

## 🌟 SlideOpsの独自性と学際的視座

従来のプレゼンテーション（PowerPoint等）は、コンテンツ（データ）とデザイン（表現）が密結合しているため、属人的なデザイン負債が発生しやすく、情報の再利用が困難でした。SlideOpsは以下の学際的アプローチにより、これらの限界を突破します。

*   **「意識させない」認知科学の自動実装**
    ユーザーが箇条書きのテキストを入力するだけで、統合されたLLM（言語モデル）が背後の文脈を読み取ります。プロスペクト理論（損失回避性の刺激）、アンカリング効果、現状維持バイアスの打破といった行動経済学的なフレームワークを自律的に適用し、最適なレイアウト構造（比較表への変換や重要指標の強調など）を決定します。
*   **強力な「ハロー効果」の常時適用**
    2026年最新のシリコンバレートレンド（True Dark、空間的ネオモーフィズム）と認知負荷を最小化するタイポグラフィをJSON定義の「デザインシステム」として中央統制します。属人的なレイアウト崩れを排除し、誰が作成しても「先進的で信頼できる」という無意識の権威性（ハロー効果）を聴衆に与えます。
*   **コンテンツの液状化とマルチユース (Docs-as-Code)**
    情報を特定のバイナリファイルにロックインせず、純粋なテキストデータとして扱います。一度記述された論理構造は、動的なHTMLスライドだけでなく、ホワイトペーパー（PDF）やWebマーケティング用のJSON-APIへと同時に、かつ柔軟に変容（液状化）します。
*   **データ駆動型の自律的進化 (Telemetry & Feedback)**
    展開されたスライドは、聴衆の滞在時間やマイクロインタラクション（クリック等の反応）を行動ログとして収集します。認知的負荷が高すぎるスライドは、次回のパイプライン実行時にAIが自律的に表現を平易化するなど、システム自体が進化するループを持ちます。

---

## 🏛️ コア・アーキテクチャ

SlideOpsは、関心事の分離（Separation of Concerns）に基づき、3つのレイヤーで構成されます。

### Layer 1: Source Layer（真実の源泉・データ定義）

人間が直接編集する唯一の層です。視覚・心理的な指定は一切行いません。

*   **`content.md` (Markdown):** プレゼンテーションの純粋なテキスト情報と論理構造（H1, リストなど）。
*   **`context.yaml` (YAML):** ターゲット聴衆（例：製造業CFO）、目的（サンクコスト打破）、想定されるトーンなどの文脈メタデータ。
*   **`design_system.json` (JSON):** 認知科学に基づき最適化されたカラースキーム、可変フォント（Variable Fonts）のスタック、フィボナッチ数列に基づく余白定義など、ブランドの視覚ルールセット。

### Layer 2: Pipeline Layer（AIオーケストレーションと生成）

Git Pushをトリガーに稼働する「認知と表現の変換」パイプラインです。

*   **AI Architect Agent:** LLMが `content.md` と `context.yaml` を解析し、最適な心理的アプローチを付与した構造化データ（`structure.json`）を生成します。同時に、ターゲット言語（en, zh-TW等）への文化的背景を考慮した翻訳（i18n）を実行します。
*   **Generator Engine:** AstroやTailwind CSSを用い、生成された構造データと `design_system.json` を動的に結合してHTML/CSSをレンダリングします。高い処理流暢性（Processing Fluency）を生むアニメーションもここで付与されます。
*   **QA Agent:** Playwrightによるヘッドレスブラウザテストを実行し、テキストのオーバーフローやアクセシビリティ（コントラスト比）の欠陥を検知・自己修復します。

### Layer 3: Delivery & Telemetry Layer（配信と動的評価）

生成された成果物を展開し、フィードバックを収集する層です。

*   **マルチエクスポート:** Netlify等のエッジネットワークへのHTML展開と同時に、マーケティングツール向けのAPIエンドポイントへデータをPushします。
*   **テレメトリ (行動ログ):** スライドごとの滞在時間が閾値を超えた場合（認知的負荷の増大と推定）や、インタラクションが少ない場合、そのデータをオーケストレータへ還流させ、プロンプトの動的調整に利用します。

---

## 🔄 運用ワークフロー

SlideOpsの導入により、プレゼンテーション作成にかかる業務フローは極限まで洗練されます。

1.  **Drafting (起草):** 担当者はデザインや見栄えを一切気にせず、Markdownで「何を伝えるか」というメッセージの論理のみを執筆します。
2.  **Committing (登録):** 完成したMarkdownと文脈（YAML）をGitリポジトリにコミットします。**（人間の手作業はここで完全に終了します）**
3.  **Automated Structuring (自動構築):** バックグラウンドでn8n等のオーケストレータが起動し、AIが心理的・視覚的に最適化されたデータ構造へと変換、多言語化を行います。
4.  **Building & Testing (生成とテスト):** 静的サイトジェネレータが最新デザインのHTMLをビルドし、自動QAテストをパスさせます。
5.  **Deployment (公開):** わずか数分以内に、学際的アプローチで設計されたプレゼンテーション用URLが発行され、即座にプレゼンや共有が可能になります。

---

## 🎨 視覚言語と認知パレット (SlideOps v1.0 Design)

フレームワークに標準搭載される視覚言語は、2026年のシリコンバレー基準（OLED最適化、空間的ネオモーフィズム）と認知心理学を融合させています。

*   **True Dark Background (`#030712`):** 眼精疲労を防ぎ、前面の情報を空間に浮かび上がらせる漆黒の背景。
*   **シグナルカラーによる感情操作:**
    *   信頼と権威性を象徴するコグニティブ・インディゴ（`#6366F1`）。
    *   損失回避性を痛切に刺激しつつ洗練を保つサーマル・ローズ（`#F43F5E`）。
*   **タイポグラフィ:** 定量データの説得力を高めるTabular Numbers（等幅数字）の設定や、遠目からでも誤読を防ぐユニバーサルデザインフォントの動的バインディング。

---

## 🚀 まとめ：SlideOpsがもたらすパラダイムシフト

SlideOpsは、単なる「スライド自動生成ツール」ではありません。

プレゼンテーション作成にかかる無駄な調整時間を「ゼロ」にし、人間のリソースを「戦略の構築」という本質的な知的生産のみに集中させます。そして、システムが自動的に認知科学と行動経済学のベストプラクティスを補完することで、**組織の誰もが、世界最高水準の説得力を持つプレゼンテーションを再現性高く生み出せる**ようになります。

SlideOpsは、企業の意思決定スピードとコミュニケーションの質を根本から変革する、真のプラットフォームエンジニアリングの実践です。
