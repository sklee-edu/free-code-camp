Free Code Camp

# Basic CSS
## Selector
h1 {

}

.class {

}

#id {

}

[attr=val] {

}

## Css precedence
Inline > ID > Class
CSS 파일은 top to bottom으로 읽으므로 아래 있는 것이 우선순위
!important를 통해서 강제 우선순위 할당

## Color
black = #000000(hex code) = #000(abbreviate hex code) = rgb(0, 0, 0)

## CSS variables
declaration: —variable-something: black
call: var(—variable-something, gray), gray같은 경우 fallback value

## CSS compatiblity
background: red;
background: var(—variable-red, red);
똑같은 background를 2개를 선언해주는 방식으로 css variable이 작동하지 않는 곳에서 compatiblity를 높임

## Cascading CSS
:root {

} 에서 선언한 variable은 cascading 되어서 다른 다양한 곳에서 사용할 수 

## media query
@media (max-width: 350px) {
	:root {
		/* add code below */
		/* add code above */
	}
}