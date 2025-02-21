---
published: true
layout: bookpage_ja-JP
weight: 48
section: Workflow
title: 発音区別符号とアクセント記号
---
[発音区別符号](../ja-JP/Glossary.md#diacritics-発音区別符号)は、文字に追加されたまたは結びついた記号で、しばしば記号を付けた文字の音価を変更するために用いられます。発音区別符号の幾つか（「アキュート」とか「グラーヴ」）はアクセント記号と呼ばれることもよくあります。発音区別記号は文字の上または下、文字上、あるいは二つの文字の間に現れます。

<img width="5%" src="../en-US/images/dia_a_grave.png"/>
<img width="5%" src="../en-US/images/dia_a_circumflex.png"/>
<img width="5%" src="../en-US/images/dia_a_tilde.png"/>
<img width="5%" src="../en-US/images/dia_a_dieresis.png"/>
<img width="5%" src="../en-US/images/dia_c_ogonek.png"/>
<img width="5%" src="../en-US/images/dia_c_cedilla.png"/>
<img width="5%" src="../en-US/images/dia_c_dot.png"/>
<img width="5%" src="../en-US/images/dia_g_comma.png"/>
<img width="5%" src="../en-US/images/dia_hungarumlaut.png"/>


### 発音区別符号の例

<p class="imagebox"><img src="../en-US/images/dia_a_grave.png"/></p>

小文字の「グラーヴ付き a」（unicode u+00e0）。小文字「a」のグリフ（unicode u+0061）と「組み合わせグラーヴ・アクセント<sup>※</sup>」のグリフ（unicode u+0300）とを組み合わせたフォントです。　《※ 訳注： 仏語＝アクサングラーヴ（重アクセント）》

<p class="imagebox"><img src="../en-US/images/dia_a_circumflex.png"/></p>

小文字の「シルコンフレックス付き a」（unicode u+00e2）。小文字「a」のグリフ（unicode u+0061）と「組み合わせシルコンフレックス・アクセント<sup>※</sup>」のグリフ（unicode u+0302）とを組み合わせたフォントです。　《※ 訳注： 仏語＝アクサンシルコンフレックス（曲折アクセント）》

<p class="imagebox"><img src="../en-US/images/dia_c_ogonek.png"/></p>

小文字の「オゴネク付き a」（unicode u+0105）。小文字「a」のグリフ（unicode u+0061）と「組み合わせオゴネク<sup>※</sup>」のグリフ（unicode u+0328）とを組み合わせたフォントです。　《※ 訳注： ポーランド語＝ogonek（しっぽ）》

<p class="imagebox"><img  src="../en-US/images/dia_c_cedilla.png"/></p>

小文字の「セディーユ付き c」（unicode u+00e7）。小文字「a」のグリフ（unicode u+0063）と「組み合わせセディーユ<sup>※</sup>」のグリフ（unicode u+0327）とを組み合わせたフォントです。　《※ 訳注： 仏語＝セディーユ》

<p class="imagebox"><img  src="../en-US/images/dia_hungarumlaut.png"/></p>

小文字の「二重アキュート付き o」（unicode u+0151）。小文字「o」のグリフ（unicode u+006f）と「組み合わせ二重アキュート・アクセント<sup>※</sup>」のグリフ（unicode u+030b）とを組み合わせたフォントです。　《※ 訳注： 仏語＝アクサンアキュート（鋭アクセント）》

<hr>

FontForge はアクセント記号付き文字を次の二つの方法で自動的に作成できます。

1. FontForge には、発音区別記符号を配置する場所に関する基本的な情報が含まれているため、ほとんどのアクセント付き文字を自動的に作成できます。

2. 発音区別符号の配置をより細かく制御するために、FontForge はユーザーが作成したアンカー・ポイントの位置に基づいて発音区別符号を配置できます。

<p class="note">ここでは次のことに留意してください：　もしアンカー・ポイントも発音区別符号の表示位置検索テーブルも使用していない場合、フォントに発音区別符号のグリフが存在していないときには、Fontforge は代わりに類似のスペース文字を使用します。たとえば、組み合わせ記号の「アキュート（acutecomb<sup>※</sup>）」（u+0301）が存在していない場合、FontForge は自動的にアキュート・アクセント記号付きグリフを生成する、標準の「アキュート文字（acute）」（u+00b4）を用います。組み合わせ記号の「アキュート（acutecomb）」（u+0301）が存在していれば、明確に「アクセント記号付きグリフの生成にはスペース文字を使用する」と指定しない限り、FontForge は常にそれを使用します。</p>

<div class="note"><p>《※ 訳注： 組み合わせグリフの場合、グリフ名の最後に「-comb」を付けることが多いようです。》</p></div>

## FontForge の「発音区分記号」自動配置の基本

FontForge の **エレメント** メニューには、アクセント記号付き文字、合成文字（composite characters）、複写文字（duplicate characters）などの作成に用いられる **組み立て** （構築）機能があります。アクセント記号付き文字を自動で作成するためには、FontForge のメニュー項目から「**エレメント** ⇒ **組み立て（U）** ⇒ **アクセントつきグリフを構築（B）**」機能を選択します。この機能は、キー入力の「<kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>A</kbd>」からも呼び出すことができます。「a acute（アキュート付き a）」文字の作成を例にとると、作成済みの小文字「a」（u+0061）と「acutecomb」（u+0301）のグリフが必要です。「a acute」文字スロットを選択、メニューの「**エレメント** ⇒ **組み立て（U）** ⇒ **アクセントつきグリフを構築（B）**」機能を使用して、小文字の「a」グリフへの参照と「acutecomb」グリフへの参照を「a acute」文字のスロットに配置します。（以下を参照）。

<img src="../en-US/images/dia_auto_a_acute.png"/>

この発音区別符号の自動配置は **環境設定** で調節可能です。設定は、メニュー項目の「**ファイル** ⇒ **環境設定** ⇒ **アクセント**」にて見つけられます（以下を参照）。

<img src="../en-US/images/preferences_accents.png" />

「**幅のあるアクセントを優先**」が「オン」設定では、たとえ適切な組み合わせ文字が存在していたとしても、アクセント記号付きグリフをスペース文字を用いて作成します。この設定は、アンカーを使って発音区分符号の位置を指定している場合は無視されます。

「**アクセント間隔の百分率**」は、文字グリフと記号グリフの間の垂直方向のスペース量を制御しています。ここに入力する値は、フォントの「[エム](../ja-JP/Glossary.md#em-エム)・スクエア」の割合です。たとえば、「6」の場合は、記号グリフを、そのフォントのエム・スクエアの６％分だけ文字グリフからずらします。

記号グリフの水平位置に関する環境設定も行なえます。「**アクセントの底を中心に**」の設定を「オン」にすると、アクセント記号のグリフは文字グリフの最低点の中央に配置されます。

「**文字の頂点を中心に**」の設定が「オン」の場合は、アクセント記号は文字グリフの最高点の中央に配置されます。

上記二つの設定を「オフ」にすると、アクセント記号は文字グリフ幅の中央に配置されます。両方ともに「オン」に設定されていると、アクセント記号は文字スロット幅の中央に配置されます。

## 発音区分符号の配置にアンカーを使用する

FontForge でアクセント記号付き文字を最も正確かつ効率的に作成する方法は、「アンカー・ポイント」を使用することです。

アンカー・ポイントを使用すると、アクセント記号付き文字の文字グリフに対する発音区分符号の位置を、正確に微調整できます。たとえば、「オゴネク付き a」の場合、「a」の文字グリフは通常の位置に配置され、「オゴネク」記号のグリフは、記号グリフのアンカー・ポイントが、文字グリフのアンカー・ポイントに一致するように配置されます。

「オグノク付き a」文字を作成する次の事例では、「基底（bottom）」と呼ばれるアンカー・クラスが作られます。小文字の「a」のグリフに、「基底」アンカーが「a」の縦線の最下部（基底部）に置かれます。これがアンカーの「基本グリフ」形です。

<img src="../en-US/images/dia_a_anchor.png"/>

「オゴネク」グリフでは、「基底」アンカーは、「記号」アンカーの形で、オゴネク・グリフの最上端（天辺）にあります。

<img src="../en-US/images/dia_ogonek_anchor.png"/>

そこで、「オゴネク付き a」文字を（「**エレメント** ⇒ **アクセントつきグリフの構築**」メニューを使用して）形成すると、記号グリフの「基底」アンカー・ポイントが文字グリフの「基底」アンカー・ポイントと同じ位置になることで、「オゴネク」のグリフが「a」グリフの縦線の基底部に正しく配置されます。この正確で自動的なグリフの配置は、文字グリフと記号グリフを配置にアンカー・ポイントの利用なくしては実現不可能でした。

<img src="../en-US/images/dia_a_ogonek_anchors.png" />

### 発音区別符号用のアンカー・ポイントを作成する（Mark-to-Base）

FontForge は「mark-to-base（符号を基底部に）」として知られている検索機能を使用してアンカー・ポイントの作成と位置合わせを行なっています。この「mark-to-base 検索」は **フォント情報** 内の「GPOS Lookups」で作成・編集できます（メニュー項目から **エレメント** ⇒ **フォント情報** ⇒ **Lookups**項目 ⇒ **GPOS**タブ の順に辿ります。 

「Lookups（検索）」項目の「**GPOS**」タブ画面で、「**Add Lookup**（検索を追加）」ボタンを押し、「**Mark to Base Position**（基底部に合わせる）」を選択し、次に「**機能**」欄の「&lt;NEW&gt;」をクリックして「**mark マークの位置指定**」を選択します。「OK」ボタンを押してウィンドウ画面を閉じます。

<img src="../en-US/images/dia_new_mark_to_base_1.png"/>

新しく作成した「検索」を選択して、「**Add Subtable**」（サブテーブルを追加）ボタンをクリックします。表示されたウィンドウで、「アンカー・クラス」を作成できます。

<img src="../en-US/images/dia_anchor_new_subtable.png" />

次の事例では、「上部 Top」と「基底部 Bottom」、二つのアンカー・クラスを作成しました。「上部」のアンカー・クラスはグリフの上側、「基底部」アンカーはグリフの下側、にある発音区別符号の配置に用いられます。

<img src="../en-US/images/dia_marks_classes_add.png" />

グリフにアンカーを付けるには、**グリフ編集ウィンドウ**（＝アウトラインウィンドウ）の中でマウスを右クリックし、表示されるメニューから「**アンカーを追加**」を選択するだけです。
表示されるダイアログ・ボックスでは、アンカーが「基底アンカー」なのか「記号アンカー」なのかを指定できます。また、アンカーの位置もこｎダイアログ・ボックスで微調整が可能です。別の方法としては、マウスでドラッグしたり矢印キーを使って、所定の場所へ移動できます。アンカー・ポイントは、また、その上を右クリックし、マウスのクリック・メニューの「**情報を得る**」を選択すると編集できます。

### アンカー・クラスの制御

FontForge には、アンカー・ポイントの全クラスの位置を制御するための便利なグラフィカル・インターフェースもあり、たとえばフォントの全てのアキュート・アクセント記号の位置を即座に、あるいは小文字の「e」を参照する文字に含まれているクラスの全てのアンカーを、微調整できたりします。下にある二つの事例では、フォント中のすべてのアキュート・アクセントの位置と、小文字「e」のグリフを参照しているすべての文字のアンカーのクラスの微調整に、このグラフィカル・インターフェースをどのように用いるかを見ることができます。　《※ 訳注：　この部分、内容的に重複しています。》

一度「mark-to-base 位置検索」にアンカー・クラスを作成し、アンカーをグリフに追加すると、そのクラスはメニュー項目の **エレメント** ⇒ **フォント情報** ⇒ **Lookups** ⇒ **GPOS** から管理でき、アンカー・クラスが格納されているサブテーブルを編集できます。表示されるのは以下のウィンドウです。

<img src="../en-US/images/dia_anchor_control_1.png" />

このウィンドウから、編集したいクラスを選択し、**アンカーの制御** ボタンをクリックします。すると、そのクラスのグラフィカル・インターフェースが表示されます。以下の事例では、「上部 Top」クラスの制御内容を編集しています。最初の例は、（ウィンドウ左・一番上の）ドロップダウン・メニューで「基底」を指定し、小文字「e」を選択したものです。基底となる文字グリフが選択されると、そのグリフを参照し、「上部」の記号アンカーを含むすべての文字がプレビュー欄に表示されます。そこで、「上部」アンカーの位置を調整すれば、それが「上部」記号アンカーを含むすべてのグリフの位置にどのように影響するかを確認することができます。

<img src="../en-US/images/dia_anchor_control_e.png" />

二番目の例は、ドロップダウン・メニューで「マーク」を指定し、「アキュート」グリフを選択した場合です。記号グリフを選択すると、その記号グリフを参照し、「上部」記号アンカーを含むすべてのグリフがプレビュー欄に表示されます。

<img src="../en-US/images/dia_anchor_control_mark.png" />


## 発音区別符号に関するその他の情報サイト

* [Context of Diacritics](http://urtd.net/projects/cod/about)「発音区別符号の前後関係」　《※ 訳注：リンク切れ。[参考1](https://typedrawers.com/discussion/409/context-of-diacritics)、[参考2](https://www.setuptype.com/blog/context-of-diacritics)》
* [On Diacritics](http://ilovetypography.com/2009/01/24/on-diacritics/)「発音区別符号について」
* [Diacritics Project @ Typo.cz](http://diacritics.typo.cz/)「発音区別符号プロジェクト」
* [Problems of diacritic design for Latin script text faces](http://scripts.sil.org/ProbsOfDiacDesign)「ラテン文字テキストの発音区別符号デザインの問題」
* [Diacritics Design Standards (for Latin based languages)](http://www.microsoft.com/typography/developers/fdsspec/diacritics.htm)「発音区分符号のデザイン標準 (ラテン文字準拠の言語用)」　《※ 訳注：リンク切れ。[参考](https://learn.microsoft.com/en-us/typography/develop/character-design-standards/diacritics)》
* [Dave Foster on Æ's](https://twitter.com/fostertype/status/610292546971893760)「&AElig; について（ツィッター）」