﻿---
title: Category Chart のカスタム ツールチップ
_description: Ignite UI for Angular Category Chart コンポーネントは、カテゴリ データを表示するタッチ対応、高いパフォーマンス、軽量なチャート コントロールです。
_keywords: Ignite UI for Angular, データ ビジュアライゼーション, UI コントロール, Angular ウィジェット, web ウィジェット, UI ウィジェット, Angular, ネイティブ Angular コンポーネント スィート, ネイティブ Angular コントロール, ネイティブ Angular コンポーネント ライブラリ, Angular Chart コンポーネント, Angular Category Chart コンポーネント, Angular Chart コントロール, Angular Category Chart コントロール
_language: ja
---
## カスタム ツールチップ

igxCategoryChart は、各シリーズ タイプにデフォルト ツールチップを提供します。デフォルト ツールチップは特定のシリーズ項目に関連するすべての情報を表示します。これはシリーズ タイトル、データ値、および軸値を含みます。シリーズのスタイルと一致します。デフォルト ツールチップのコンテンツおよびルック アンド フィールを変更するためにカスタム ツールチップを構成できます。

<div class="divider"></div>

### カスタム ツールチップ デモ

<div class="sample-container" style="height: 650px">
    <iframe id="category-chart-custom-tooltips-iframe" src='{environment:demosBaseUrl}/category-chart-custom-tooltips' width="100%" height="100%" seamless frameBorder="0" onload="onSampleIframeContentLoaded(this);"></iframe>
</div>
<div>
    <button data-localize="stackblitz" class="stackblitz-btn"   data-iframe-id="category-chart-custom-tooltips-iframe" data-demos-base-url="{environment:demosBaseUrl}">StackBlitz で開く
    </button>
</div>

<div class="divider--half"></div>

TODO - UPDATE CONTENT AND CODE SNIPPET

ツールチップ コンテンツは `seriesAdded` イベントでカスタマイズされます。

```html
<igx-category-chart
    [dataSource]="data"
    width="700px"
    height="500px"
    >
</igx-category-chart>
```


