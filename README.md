# Codykit
scss style sets

## function
### 미디어 쿼리 보기
```scss
	@include codykit-media-trace();
```

### 자식이 부모 태그 셀렉터 수정
```scss
span.badge {
	@include when("span.badge",".badge-red"){
		color:red;
	}
	@include when("span.badge",".badge-blue"){
		color:blue;
	}
}

### 간단한 포커싱
```scss
div {
	@include focus(red);
}
```

### absoulte를 쉽게
```scss
cover {
	position:relative;
	section {
		@include absolute(right,10px);
	}
}

```

### scroll bar style (only webkit)
```scss
screen {
	@include scrollbar-variant
}
```


### media setting
```scss
@import 'codykit';
@include codykit-media-width(480px,768px,992px,1200px);

body > section {
	@include media-mobile {
		width:400px;
	}
	@include media-tablet {
		width:700px;
	}
	@include media-desktop {
		width:1028px;
	}
}
```


### response column
```scss

inventory.no-media {
	// gap 10px;
	@include response-section(10px);
	flow {
		//3column
		@include response-column(100%/3);
	}
}


inventory.with-media {
	// gap 10px;
	@include response-section(10px);
	flow {
		//1column
		@include media-mobile {
			@include response-column(100%);
		}
		//2column
		@include media-tablet {
			@include response-column(50%);
		}
		//4column
		@include media-desktop {
			@include response-column(50%);
		}
	}
}
```









### icon (background base icon)
```scss
span {
	@include icon-variant(url(icon.png),10px,10px);
}
```

### image text (inline)
```scss
span {
	@include image-text-variant(url(word.png),20px,10px);
}
```


### easy input style defaultlize
```scss
input {
	@mixin input-variant(20px,100px){
		color:gray;
		background-color:white;
	}
}
```









## Basic custom tag

#### group tag
tag | description 
--- | -----------
content | header,footer외의 컨텐츠 요소의 부족한 정의 보충
cover | 단지 스타일을 위한 껍데기를 나타내는 태그
frieze | 섹션이나 컨텐츠의 동질적이거나 연속적인 구간을 나누기 위한 장식 또는 구간
bar | 섹션의 중간에 위치한 유틸리티 그룹
group | 헤더 요소가 있는 작은 그룹
context | 필요에 의해 위치가 변경되는 그룹
controls | 관련있는 복수의 ui요소의 합집함

#### utility tag
tag | description 
--- | -----------
inventory, flow | 어떠한 주제에 대한 컬랙션을 나타냄. flow는 커버 역활이다
item | 데이터 하나를 나타내는 태그
part | 조립 가능한 부분적이고 반복적인 '스타일요소'
band | 여러 태그 단위를 하나의 의미로 묶은 컨텐츠
sign | 내용이 없는 시각적 컨텐츠
switch, case | 상태에 따라 보여질수 있는 '기능요소'
modal  | dialog등의 사용의 흐름을 막는 스테이지 요소
screen | 스크롤 가능한 컨텐츠 랩퍼
noscreen | 스크롤 불가한 영역을 나타냄
nocontent | 컨텐츠가 없을때 나타내는 내용

#### inline tag
tag | description 
--- | -----------
detail | 섹션 단위의 히든 컨텐츠
message | 메시지 단위의 히든 컨텐츠
badge | 토큰 단위의 그룹화된 텍스트 컨텐츠
unit | 단위를 나타냄 (var의 도움 태그)
om | 개행될수 없는 텍스트 컨텐츠를 나타냄

### content
Section complementary element

```html
<section>
	<header></header>
	<content></content>
	<footer></footer>
</section>
```


### content
```html
<main>
	<header>
	</header>
	<content>
		<cover class="white-box">
			...
		</cover>
	</content>
</main>
```


### frieze
```html
<content>
	<frieze>
		<header>Middle titte1</header>
		<content>
		...
		</content>
	</frieze>
	<frieze>
		<header>Middle title2</header>
		<content>
		...
		</content>
	</frieze>
</content>
```


### bar
Piece content element
```html
<bar>
	Info messege
</bar>

or


<content>
	<bar>
		<select>
			<option>2column</option>
			<option>3column</option>
		</select>
		<button>submit</button>
	</bar>
	<table>
		<thead>...</thead>
		<tbody>...</tbody>
	</table>
</content>
```


```

```
### inventory, flow, item
Column list content element
```html
<inventory>
	<flow>
		<item>
			Item 1
		</item>
	</flow>
	<flow>
		<item>
			Item 2
		</item>
	</flow>
</inventory>
```
### group
```html
<group>
	<header>
		This is chart.
	</header>
	<band>
		<some-graphic></some-graphic>
		<some-graphic></some-graphic>
	</band>
	<sign>
		<p class="legend"></p>
	</sign>
</group>
```
### context, group, controls
Form factor element
```html
<section>
	<context>
		<group>
			<header>...</header>
			<controls>
				<button>Command1</button>
				<button>Command2</button>
			</controls>
		</group>
	</context>
</section>
```
### switch, case
Switch content element
```html
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
<noscreen>
	<table><thead></thead></table>
</noscreen>
<screen>
	<table><tbody></tbody></table>
</screen>
```