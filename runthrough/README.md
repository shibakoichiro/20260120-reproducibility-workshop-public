# Run-Through Files (Quarto Manuscripts Project)

ワークショップの Parts 3-6 のコードをそのまま統合した **Quarto Manuscripts** プロジェクトです。
ワークショップページのコードをコピペなしで実行できます。

## 構成

```
runthrough/
├── _quarto.yml              # Manuscripts プロジェクト設定
├── data-cleaning.qmd        # Part 3: データクリーニング
├── analysis.qmd             # Parts 4-5: 解析、表、図
├── index.qmd                # Part 6: 原稿（embed 構文使用）
├── results/                 # 生成された .rds ファイル
└── references.bib           # 参考文献
```

## 実行順序

**チャンクをインタラクティブに実行する場合:**

1. **data-cleaning.qmd**
   - `results/data_clean.rds` を生成

2. **analysis.qmd**
   - `data_clean.rds` を読み込み
   - 表・図を生成、`model_fit.rds` 等を保存

3. **index.qmd** を Render
   - `{{< embed analysis.qmd#... >}}` 構文で analysis から表・図を埋め込み
   - inline code で数値を動的に表示

## Render

```bash
cd runthrough
quarto render
```

Manuscripts プロジェクトなので、Render すると **全体がビルド** されます。
`index.qmd` に `analysis.qmd` の表・図が埋め込まれます。

## embed 構文の例

```markdown
# index.qmd 内

Participant characteristics are presented in @tbl-demographics.

{{< embed analysis.qmd#tbl-demographics >}}
```

この構文により、`analysis.qmd` の `#| label: tbl-demographics` チャンクの出力が原稿に埋め込まれます。

## 既知の制限事項

**gtsummary/gt テーブルの embed 問題**: 現在の Quarto Manuscripts では、gtsummary や gt パッケージで生成した表は embed ショートコードで正しく表示されません（図は正常に動作します）。これは Quarto の既知の制限です。

- **回避策**: 表を確認するには `_manuscript/analysis-preview.html` を直接開いてください
- テーブルは `analysis.qmd` 内では正しくレンダリングされます
- ワークショップでは、embed の概念を学ぶことが主目的なので、この制限は教育上問題ありません

## ラベル対応表

| Part | チャンク | ラベル |
|------|---------|--------|
| 5 | Demographics table | `tbl-demographics` |
| 5 | Box plot | `fig-bp-education` |
| 5 | Regression table | `tbl-regression` |
| 5 | Subgroup forest plot | `fig-subgroup` |
