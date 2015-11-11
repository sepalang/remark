# Codykit
scss style sets

## Basic custom tag
### content
Section complementary element

```html
<section>
	<header></header>
	<content></content>
	<footer></footer>
</section>
```
### leaf
Hidden content element
```html
<leaf>
	Info messege
</leaf>
```
### inventory, deck, item, sign
List content element
```html
<inventory>
	<deck>
		<item>
			<header>
				Item title
			</header>
			<sign>
				(Visual factor)
			</sign>
		</item>
	</deck>
</inventory>
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