﻿---
title: Label および Input ディレクティブ
_description: Ignite UI for Angular Label および Input ディレクティブを使用すると、単一行または複数行のテキスト要素を作成し、CSS スタイルを追加し、その他のコントロールと統合できます。
_keywords: Ignite UI for Angular, UI コントロール, Angular ウィジェット, web ウィジェット, UI ウィジェット, Angular, ネイティブ Angular コンポーネント スィート, ネイティブ Angular コントロール, ネイティブ Angular コンポーネント ライブラリ, Angular Label コンポーネント, Angular Label コントロール, Angular Input コンポーネント, Angular Input コントロール, Input コンポーネント, Input コントロール, Label コンポーネント, Label コントロール, Angular Input ディレクティブ, Angular Label ディレクティブ, Angular Forms, Angular Reactive Forms, Angular フォームの検証
_language: ja
---

## Label および Input
<p class="highlight">
Ignite UI for Angular Input および Label ディレクティブを使用すると、単一行または複数行のテキスト要素を作成できます。フォーム入力の全般的なシナリオにおいて便利な機能です。
</p>
<div class="divider--half"></div>

### Label および Input デモ
<div class="sample-container" style="height:100px">
<iframe id="input-group-sample-2-frame" src='{environment:demosBaseUrl}/input-group-sample-2' width="100%" height="100%" seamless frameBorder="0"></iframe>
</div>
<div>
    <button data-localize="stackblitz" class="stackblitz-btn" data-iframe-id="input-group-sample-2-frame" data-demos-base-url="{environment:demosBaseUrl}">StackBlitz で開く</button>
</div>
<div class="divider--half"></div>

### 使用方法
Label および Input ディレクティブのデフォルト スタイル設定はマテリアル デザイン [**ガイドライン**](https://material.io/guidelines/components/text-fields.html)のテキスト フィールド仕様を実装します。

> [!NOTE]
> `igxInput` および `igxLabel` を使用するには、`<igx-input-group>` コンテナーにラップする必要があります。

Ignite UI for Angular Label および Input を初期化する前に、**IgxInputGroup** を **app.module.ts** ファイルにインポートします。

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

### Label および Input
HTML ラベルおよび入力は HTML フォームの基本要素です。`igxLabel` および `igxInput` ディレクティブの使用例:

```html
<igx-input-group>
    <input igxInput name="fullName" type="text" />
    <label igxLabel for="fullName">Full Name</label>
</igx-input-group>
```

結果は以下です。

<div class="sample-container" style="height:100px">
<iframe id="input-group-sample-1-frame" src='{environment:demosBaseUrl}/input-group-sample-1' width="100%" height="100%" seamless frameBorder="0"></iframe>
</div>
<div class="divider--half"></div>

`igxInput` ディレクティブを `<input>` および `<textarea>` HTML 要素に適用できます。単一行および複数行テキスト フィールドをサポートします。

#### 検証
Ignite UI for Angular Input ディレクティブで検証が有効な場合にマテリアルに基づくスタイル設定を提供します。入力に `required` 属性を追加します。

```html
<igx-input-group>
    <input igxInput name="fullName" type="text" required="required" />
    <label igxLabel for="fullName">Full Name</label>
</igx-input-group>
```

以下のコード例およびデモは、検証に成功または失敗するかどうかに基づいてラベルの隣にあるアスタリスクを表示し、入力が緑または赤くなることを確認できます。

<div class="sample-container" style="height:100px">
<iframe id="input-group-sample-2-frame" src='{environment:demosBaseUrl}/input-group-sample-2' width="100%" height="100%" seamless frameBorder="0"></iframe>
</div>
<div class="divider--half"></div>

#### データ バインディング
Ignite UI for Angular Input は one-way および two-way データ バインディングをサポートします。入力に両方向のデータ バインディングを追加します。以下はコンポーネントのコード:

```typescript
public user = {
    fullName: ""
};

```

マークアップのコード:

```html
<igx-input-group>
    <input igxInput name="fullName" type="text" [(ngModel)]="user.fullName" required="required" />
    <label igxLabel for="fullName">Full Name</label>
</igx-input-group>
```

### Input Group
Input Group コンポーネントの詳細については[ここ](input_group.md)を参照してください。

## Input API

### 入力

|名前|型|説明|
|--- |--- |--- |
|`value`|any|入力の値。|
<div class="divider--half"></div>

### ゲッター/セッター

|名前|型|ゲッター|セッター|説明|
|--- |--- |--- |--- |--- |
|`valid`|IgxInputState|はい|いいえ|入力の検証状態。有効な値は `IgxInputState.INITIAL`、`IgxInputState.VALID`、および `IgxInputState.INVALID` です。|
|`disabled`|boolean|はい|はい|入力の `disabled` プロパティを取得または設定します。|
|`focused`|boolean|はい|いいえ|入力がフォーカスを持つかどうかを取得します。|
<div class="divider--half"></div>

## 追加のリソース
関連トピック:

* [Input Group](input_group.md)
<div class="divider--half"></div>

コミュニティに参加して新しいアイデアをご提案ください。

* [Ignite UI for Angular **フォーラム** (英語)](https://www.infragistics.com/community/forums/f/ignite-ui-for-angular)
* [Ignite UI for Angular **GitHub** (英語)](https://github.com/IgniteUI/igniteui-angular)