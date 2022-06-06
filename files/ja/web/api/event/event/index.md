---
title: Event()
slug: Web/API/Event/Event
tags:
  - API
  - Constructor
  - DOM
  - Event
  - リファレンス
  - コンストラクター
translation_of: Web/API/Event/Event
---
<div>{{APIRef("DOM")}}</div>

`**Event()**` コンストラクターは、新しい {{domxref("Event")}} を生成します。

<h2 id="Syntax" name="Syntax">構文</h2>

<pre class="syntaxbox">new Event(<var>typeArg</var>[, <var>eventInit</var>]);</pre>

<h3 id="Values" name="Values">値</h3>

<dl>
- `<var>typeArg</var>`
  - : {{domxref("DOMString")}} で、イベントの名前を表します。
- `<var>eventInit</var>` {{optional_inline}}
 <dd>`EventInit` 辞書で、以下のフィールドを持ちます。
 <ul>
  <li>`bubbles`: {{jsxref("Boolean")}} で、イベントがバブリングするかどうかを示します。既定値は `false` です。</li>
  <li>`cancelable`: {{jsxref("Boolean")}} で、イベントがキャンセル可能かどうかを示します。既定値は `false` です。</li>
  <li>`composed`: {{jsxref("Boolean")}} で、イベントがシャドウルートの外のリスナーに伝わるかどうかを示します (詳しくは {{domxref("Event.composed")}} を参照してください)。既定値は `false` です。</li>
 </ul>
 </dd>
</dl>

<h2 id="Example" name="Example">例</h2>

<pre class="brush: js">// create a look event that bubbles up and cannot be canceled

var evt = new Event("look", {"bubbles":true, "cancelable":false});
document.dispatchEvent(evt);

// event can be dispatched from any element, not only the document
myDiv.dispatchEvent(evt);
</pre>

<h2 id="Specifications" name="Specifications">仕様書</h2>

<table class="standard-table">
 <thead>
  <tr>
   <th scope="col">仕様書</th>
   <th scope="col">状態</th>
   <th scope="col">備考</th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td>{{SpecName('DOM WHATWG','#dom-event-event','Event()')}}</td>
   <td>{{Spec2('DOM WHATWG')}}</td>
   <td>初回定義</td>
  </tr>
 </tbody>
</table>

<h2 id="Browser_compatibility" name="Browser_compatibility">ブラウザーの互換性</h2>

{{Compat("api.Event.Event")}}

<h2 id="See_also" name="See_also">関連情報</h2>

<ul>
 <li>{{domxref("Event")}}</li>
 <li>{{domxref("EventTarget.dispatchEvent()")}}</li>
 <li><a href="/ja/docs/Web/Guide/Events/Creating_and_triggering_events">イベントの作成とトリガー</a></li>
</ul>