# Dialogue Essay — 対話から育てる論考

人間の思考（HI）を残し、AIが検討し、総括するためのスキルです。

「この文章を仕上げて」と頼むと、読みやすくなる一方で、人間が何を考えたのかとAIが何を補ったのかの境界が消えることがあります。このスキルは、人間が対話で示した着想と筋道を前段に残し、AIによる評価と総括を後段に置きます。

## できあがる論考

1. **導入** — 問いと、誰が着想・編集・検討を担ったか。
2. **人間の思考（HI）** — 人間の問い、仮説、理由、比喩、提案をAIが校正・編集した文章。
3. **AIの検討** — 資料の確認、支持する理由、成立条件、補強・検証の提案。
4. **AIによる総括** — 判断とその理由、一致点・相違点、次に育てる可能性。

一問一答の再現は必須ではありません。人間の論旨をまとまって展開し、各文にAIの留保を挟みません。AIが追加した推論はAIの部分に置きます。信頼性は、帰属の透明性と追える根拠によって育てます。

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

## License

スキルと本リポジトリの文書は [MIT License](LICENSE) で利用・改変・再配布できます。リンク先の記事や第三者の資料には、それぞれの権利条件が適用されます。

---

## English overview

Dialogue Essay preserves human-origin thinking (HI) in the first part, copyedited by AI, followed by the AI's own assessment and synthesis. It keeps attribution visible rather than blending the human hypothesis and the AI's qualifications into one voice.

Invoke it before an interview or retrospectively when a conversation feels worth preserving. It asks for the participant's publication name at invocation unless already supplied for the current essay. AI-added arguments belong in the AI section. The instructions are written in Japanese; essays may be produced in the requested language.

Install `skills/dialogue-essay` into your Codex skills directory, then restart Codex. Use `$dialogue-essay` with the conversation you want to develop. Distributed under the MIT License.
