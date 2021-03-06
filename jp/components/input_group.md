﻿---
title: Input Group コンポーネント
_description: Ignite UI for Angular Input Group コンポーネントを使用すると、単一行または複数行のテキスト要素を作成し、CSS スタイルを追加し、その他のコントロールと統合できます。
_keywords: Ignite UI for Angular, UI コントロール, Angular ウィジェット, web ウィジェット, UI ウィジェット, Angular, ネイティブ Angular コンポーネント スィート, ネイティブ Angular コントロール, ネイティブ Angular コンポーネント ライブラリ, Angular Label コンポーネント, Angular Label コントロール, Angular Input コンポーネント, Angular Input コントロール, Input コンポーネント, Input コントロール, Label コンポーネント, Label コントロール, Angular Input Group コンポーネント, Angular Input Group コントロール, Angular Input ディレクティブ, Angular Label ディレクティブ, Angular Forms, Angular Reactive Forms, Angular フォーム検証
_language: ja
---

## Input Group
<p class="highlight">
Ignite UI for Angular Input Group コンポーネントを使用すると、単一行または複数行のテキスト要素を作成できます。Label、Input、Suffix、Prefix、および Hint ディレクティブと使用すれば、フォーム入力の全般的なシナリオを実装できます。
</p>
<div class="divider--half"></div>

### Input Group デモ
<div class="sample-container" style="height:600px">
<iframe id="input-group-sample-6-frame" src='{environment:demosBaseUrl}/input-group-sample-6' width="100%" height="100%" seamless frameBorder="0"></iframe>
</div>
<div>
    <button data-localize="stackblitz" class="stackblitz-btn" data-iframe-id="input-group-sample-6-frame" data-demos-base-url="{environment:demosBaseUrl}">StackBlitz で開く</button>
</div>
<div class="divider--half"></div>

### 使用方法
Input Group コンポーネントおよびその関連するディレクティブのデフォルト スタイル設定はマテリアル デザイン [**ガイドライン**](https://material.io/guidelines/components/text-fields.html)のテキスト フィールド仕様を実装します。

Ignite UI for Angular Input Group、Input、Label、Prefix、Suffix、および Hint を初期化する前に、最初に **IgxInputGroup** を **app.module.ts** ファイルにインポートします:

```typescript
// app.module.ts

...
import { IgxInputGroup } from 'igniteui-angular/main';

@NgModule({
    ...
    imports: [..., IgxInputGroup],
    ...
})
export class AppModule {}
```

> [!NOTE]
> `igxInput`、`igxLabel`、`igxPrefix`、`igxSuffix`、または `igxHint` ディレクティブを使用するには、`<igx-input-group>` コンテナーにラップする必要があります。

### Label および Input
`igxLabel` および `igxInput` ディレクティブ、およびその検証、データ バインディング、および API を[このトピック](label_input.md)に参照してください。

### Prefix と Suffix
入力のプレフィックスまたはサフィックスを追加するために Ignite UI for Angular Prefix または Suffix を使用できます。両方のディレクティブが HTML 要素、文字列、またはその他のコンポーネントを含むことができます。文字列 **prefix** (`+359`) および igxIcon **suffix** (`<igx-icon name="phone"></igx-icon>`) を持つ新しい入力フィールドを追加します。

```html
<igx-input-group>
    <igx-prefix>+359</igx-prefix>
    <label igxLabel for="phone">Phone</label>
    <input igxInput name="phone" type="text" [(ngModel)]="user.phone" />
    <igx-suffix>
        <igx-icon name="phone"></igx-icon>
    </igx-suffix>
</igx-input-group>
```

デモは以下のようになります。

<div class="sample-container" style="height:100px">
<iframe id="input-group-sample-3-frame" src='{environment:demosBaseUrl}/input-group-sample-3' width="100%" height="100%" seamless frameBorder="0"></iframe>
</div>
<div class="divider--half"></div>

### Hint
Ignite UI for Angular Hint は入力の下に配置されるヘルパー テキストを提供します。ヒントを入力の開始または終了に配置できます。`igxHint` の位置を `position` プロパティを使用して設定できます。phone 入力にヒントを追加します。

```html
<igx-input-group>
    <igx-prefix>+359</igx-prefix>
    <label igxLabel for="phone">Phone</label>
    <input igxInput name="phone" type="text" [(ngModel)]="user.phone" />
    <igx-suffix>
        <igx-icon name="phone"></igx-icon>
    </igx-suffix>
    <igx-hint position="start">Ex.: +359 888 123 456</igx-hint>
</igx-input-group>
```

ヒントを持つ phone フィールドは以下のようになります。

<div class="sample-container" style="height:110px">
<iframe id="input-group-sample-4-frame" src='{environment:demosBaseUrl}/input-group-sample-4' width="100%" height="100%" seamless frameBorder="0"></iframe>
</div>
<div class="divider--half"></div>

### スタイル設定
入力にスタイルを適用するには、`igxInputGroup` コンポーネントの `type` プロパティを使用します。現在 line (デフォルト)、box、border、および search のスタイル設定をサポートします。スタイル設定の結果:

<div class="sample-container" style="height:520px">
<iframe id="input-group-sample-5-frame" src='{environment:demosBaseUrl}/input-group-sample-5' width="100%" height="100%" seamless frameBorder="0"></iframe>
</div>
<div>
    <button data-localize="stackblitz" class="stackblitz-btn" data-iframe-id="input-group-sample-5-frame" data-demos-base-url="{environment:demosBaseUrl}">StackBlitz で開く</button>
</div>
<div class="divider--half"></div>

## Input Group API

### 入力

|名前|型|説明|
|--- |--- |--- |
|`type`|string|入力のスタイル方法。有効な値は `line`、`box`、`border`、および `search` です。デフォルト値は `line` です。|
<div class="divider--half"></div>

### メソッド

|構文|説明|
|--- |--- |
|`isTypeLine()`|`igxInputGroup` の `type` が `line` かどうか。|
|`isTypeBox()`|`igxInputGroup` の `type` が `box` かどうか。|
|`isTypeBorder()`|`igxInputGroup` の `type` が `border` かどうか。|
|`isTypeSearch()`|`igxInputGroup` の `type` が `search` かどうか。|
<div class="divider--half"></div>

## Hint API

### 入力

|名前|型|説明|
|--- |--- |--- |
|`position`|string|ヒントの配置。有効な値は `start` および `end` です。デフォルト値は `start` です。|
<div class="divider--half"></div>

## 追加のリソース
関連トピック:

* [Label および Input](label_input.md)
<div class="divider--half"></div>

コミュニティに参加して新しいアイデアをご提案ください。

* [Ignite UI for Angular **フォーラム** (英語)](https://www.infragistics.com/community/forums/f/ignite-ui-for-angular)
* [Ignite UI for Angular **GitHub** (英語)](https://github.com/IgniteUI/igniteui-angular)
