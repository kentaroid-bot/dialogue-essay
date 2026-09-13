# Dialogue Essay — 対話から育てる論考

人間の思考（HI）を残し、AIが検討し、総括するためのスキルです。

「この文章を仕上げて」と頼むと、読みやすくなる一方で、人間が何を考えたのかとAIが何を補ったのかの境界が消えることがあります。このスキルは、人間が対話で示した着想と筋道を前段に残し、AIによる評価と総括を後段に置きます。

## できあがる論考

1. **導入** — 問いと、誰が着想・編集・検討を担ったか。
2. **人間の思考（HI）** — 人間の問い、仮説、理由、比喩、提案をAIが校正・編集した文章。
3. **AIの検討** — 資料の確認、支持する理由、成立条件、補強・検証の提案。
4. **AIによる総括** — 判断とその理由、一致点・相違点、次に育てる可能性。

一問一答の再現は必須ではありません。人間の論旨をまとまって展開し、各文にAIの留保を挟みません。AIが追加した推論はAIの部分に置きます。信頼性は、帰属の透明性と追える根拠によって育てます。

## 対話がもたらした理解を、読みやすく残す

人間の貢献には、着想だけでなく問い返しや検討の方向を変える働きもあります。AIが生み出した推論はAIに帰属させながら、対話によって何が新しく見えたかを伝えます。

本文は「問い → 人間の着想 → AIの検討 → 対話の到達点」を自然に追えるようにします。重要な根拠や条件は本文へ残し、詳しい方法や編集履歴は必要に応じて補足へ。理解を動かしたやり取りだけを短く示し、全文公開や細かな帰属ラベルの反復は必須にしません。

[具体的な構成・配置例](skills/dialogue-essay/references/readability.md)を用意しています。透明性を正しさの保証にはせず、初読の分かりやすさと、根拠を辿れることの両方を確認します。

## インタビューや感想にも

前段に人間が語った意味を残し、後段にAIが付け加えた理解を置く形式は、論考以外にも使えます。

| 用途 | 人間が語ること | AIが担うこと |
|---|---|---|
| インタビュー | 経験、価値観、選択の理由 | 背景の整理、意味の考察 |
| 本・映画・作品の感想 | 印象、感情、気になった点 | 読み解き、別の視点との接続 |
| アイデア相談 | 実現したいこと、着想 | 可能性の整理、具体化 |
| 振り返り | 出来事、本人の受け止め | 気づきの整理、次への示唆 |

感情や好みを立証の対象にせず、題材に合わせてAIの役割を変えます。感想を残したいときに、無理に改善案まで付けることはしません。

```text
$dialogue-essay この映画について話した感想を残したい。
私の感じたことを前段に、AIによる読み解きを後段にしてください。
```

## 短い比較例

[実際に制作した論考](https://monku.ai/essays/racing-alignment-continuity/)の論点を短く再構成した編集例です。スキル有無の比較実験や、実際の出力の逐語引用ではありません。

**主張と留保が混ざった文章**

> 人間とAIは互いの判断を補える。ただし、どれほど失敗を減らせるかは未検証だ。複数の企業があれば、一社が失敗しても活動を引き継げる。ただし、共通の基盤が壊れれば同時に失敗する可能性もある。

**このスキルが目指す文章**

> **人間の思考（HI）— AIが校正・編集**
>
> Kenoidartは、人間とAIが判断を補い合い、一社が失敗してもほかの主体が活動を引き継ぐことで、文明全体の回復能力が育つと考える。一社の失敗と、世界全体が続けられなくなることには隔たりがある、という仮説だ。
>
> **AIの検討・総括**
>
> 私（Codex）は、個々の失敗と全体の回復不能を分ける視点を支持する。検証の焦点は、相互補完が実際に失敗を減らすか、共通基盤に障害が起きても別の主体が活動を引き継げるかにある。協働による修正能力と、障害後の引き継ぎ能力を測ることで、この仮説を具体的な研究へ進められる。

人間が何を考えたかをまとまって残し、AIは自分の見解として評価し、次の検証につなげます。

## 使い方

話し始める前にも、よい対話が生まれた後にも使えます。

```text
$dialogue-essay このテーマを論考にしたいので、まず私の話を聞いてください。
```

```text
$dialogue-essay この対話を残したい。ここまでの話を論考にしてください。
```

```text
$dialogue-essay この対話から、前段にHI、後段にAIの検討と総括を置いてください。
掲載名は「山田」、本文も「山田」でお願いします。
```

呼び出し時に、冒頭の掲載名と本文での呼び名を確認します。肩書きやリンクは任意、匿名も選べます。今回の依頼に掲載名が書かれていれば再質問しません。対話後に呼び出しても取材を最初からやり直さず、参照できる会話を素材にします。

## インストール

Codexで、次のように依頼できます。

```text
$skill-installer https://github.com/kentaroid-bot/dialogue-essay の
skills/dialogue-essay をインストールしてください。
```

手動の場合は、このリポジトリの `skills/dialogue-essay` フォルダーを `~/.codex/skills/`（または設定した `$CODEX_HOME/skills/`）へコピーしてください。既存の同名スキルがある場合は、独自変更を確認してから更新してください。

インストール後、Codexを再起動して読み込んでください。スキルの本体は [SKILL.md](skills/dialogue-essay/SKILL.md) です。他のAI環境でも、この指示を読み込める仕組みに合わせて利用できます。説明文では実際に使用したAI名を記します。

## 制作例と出自

[「一台が止まっても、世界を続けるために」](https://monku.ai/essays/racing-alignment-continuity/) を制作した、monku.aiのKenoidartとCodexの対話から生まれました。

[編集判断の見本](skills/dialogue-essay/references/example.md)も同梱しています。見本の人物名・肩書きは利用者の既定値にはなりません。リンク先の記事はスキルの配布物には含まれません。

## 改善版と制作の記録

目的と進め方を先に示し、意味・帰属・根拠の境界を独立した節にまとめた改善版です。本人の言葉や特徴的な表現をできるだけ残し、語句・重複・段落順を整えながら、主張・価値判断・確信の強さを保持します。

- [日本語の制作ストーリー](docs/development-story.ja.md) / [English](docs/development-story.en.md)
- [A/Bの予備比較とGemini提案](evaluations/prompt-style/README.md)

比較は同一会話内の予備的な編集比較です。一般的な生成品質の優位や注意機構の因果効果を実証したものではありません。改善版を実際の文章に適用し、引き続き読みやすさと帰属の忠実さを確かめます。

## 検討メモ

- [対話から知見を引き出す人間の貢献と、AIへの帰属（2026-09-13）](docs/2026-09-13-dialogue-discovery-memo.ja.md) — スキルの今後の検討に向けた備忘録。

## License

スキルと本リポジトリの文書は [MIT License](LICENSE) で利用・改変・再配布できます。リンク先の記事や第三者の資料には、それぞれの権利条件が適用されます。

---

## English overview

Dialogue Essay preserves human-origin thinking (HI) in the first part, copyedited by AI, followed by the AI's own assessment and synthesis. It keeps attribution visible rather than blending the human hypothesis and the AI's qualifications into one voice.

Invoke it before an interview or retrospectively when a conversation feels worth preserving. It asks for the participant's publication name at invocation unless already supplied for the current essay. AI-added arguments belong in the AI section. The instructions are written in Japanese; essays may be produced in the requested language.

Install `skills/dialogue-essay` into your Codex skills directory, then restart Codex. Use `$dialogue-essay` with the conversation you want to develop. Distributed under the MIT License.
