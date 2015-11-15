# Codykit
scss style sets


## Basic custom tag


tag | description 
--- | -----------
content | header,footer외의 컨텐츠 요소의 부족한 정의 보충 
stage | content 내부의 그래픽적 박스 묶음 단위
leaf | 시각적 박스 컨텐츠
inventory, deck, item | 컬랙션 구조 태그
part | (조립 가능한) 부분적이고 반복적인 UI요소 정의
band | ui의 단위를 하나로 묶는 역할
sign | 내용이 없는 시각적 컨텐츠
bundle | 로케이션 혹은 컨트롤러의 역활의 서브 기능 단위
context | 시각적 묶음 단위
group | 상위 기능단위의 세부적인 컨트롤 묶음
controls | 컨트롤 묶음의 컨트롤 ui
tab | 탭
switch, case | 스위치케이스
modal  | dialog등의 스테이지
screen | 스크롤 가능한 컨텐츠 랩퍼

### content
Section complementary element

```html
<section>
	<header></header>
	<content></content>
	<footer></footer>
</section>
```
### stage
```html
Detail box
<content>
	<stage>
		stage1
	</stage>
	<stage>
		stage2
	</stage>
</content>
```

### leaf
Piece content element
```html
<leaf>
	Info messege
</leaf>
```
### inventory, deck, item
Column list content element
```html
<inventory>
	<deck>
		<item>
			Item 1
		</item>
	</deck>
	<deck>
		<item>
			Item 2
		</item>
	</deck>
</inventory>
```
### UI group
```html
<part>
	<band>
		<some-graphic></some-graphic>
		<some-graphic></some-graphic>
	</band>
	<sign>
		<p class="legend"></p>
	</sign>
</part>
```
### bundle, context, group, controls
Form factor element
```html
<bundle>
	<context>
		<group>
			<header>
				Control group title
			</header>
			<controls>
				<button>Command1</button>
				<button>Command2</button>
			</controls>
		</group>
	</context>
</bundle>
```
### tab, switch, case
Switch content element
```html
<tab>
	<li><a>Item1</a></li>
	<li><a>Item2</a></li>
	<li><a>Item3</a></li>
</tab>
<switch>
	<case>
		Case content 1
	</case>
	<case>
		Case content 2
	</case>
	<case>
		Case content 3
	</case>
</switch>
```
### modal
Dialog stage element
```html
<modal>
	<dialog>
		<header>title</header>
		<content>modal content</content>
		<footer>
			<controls>
				<button>cancle</button>
				<button>ok</button>
			</controls>
		</footer>
	</dialog>
</modal>
```
### screen
Scroll content element
```html
<screen>
	Screen content
</screen>
```