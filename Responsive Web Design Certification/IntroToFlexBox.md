# Introduction to the CSS Flexbox Challenges

# For flex container
## CSS Flexbox
parent는 flex container가 될 수 있음
child들은 flex item이 됨
```css
display: flex;
```

## Flex direction
parent는 child의 flex direction을 설정할 수 있음
flex-item들이 어떤 순서로 배치될 것인지에 대한 것임(main axis)
기본 값은 row
```css
flex-direction: row-reverse;
```

## Justify content
parent의 main axis에 따라 어떻게 flex item들을 배치(space out)할 것인지에 대한 것
```css
justify-content: [flex-start, flex-end, space-between, space-around, center]
```

## Align items
parent의 cross axis에 따라 어떻게 flex item들을 배치할 것인지에 대한 것
```css
align-items: [flex-start, flex-end, center, stretch, baseline]
```

## Flex wrap
parent가 flex-item들을 한 줄이 아니라 여러 줄에 걸쳐서 가지게 함
```css
flex-wrap: [nowrap, wrap, wrap-reverse]
```

# For Flex items
## Flex shrink
shrink 값이 큰만큼 더 많이 줄어듬.
2가 1보다 더 많이 줄어듬
```css
flex-shrink: 2;
```

## Flex grow
grow 값이 큰만큼 더 많이 커짐.
2가 1보다 더 큼
```css
flex-grow: 2;
```

## Flex basis
grow, shrink가 없을 때의 기본 값
```css
flex-basis: 10em;
```

## Flex 
grow, shrink, basis 순서대로 배치함
```css
flex: 1 1 150px;
```

## Order
flex item들의 순서를 배치해줌
```css
order: 1;
```

## Align self
flex item은 float, clear, vertical-align 등이 작동하지 않음
parent의 align-items를 override 함
``` css
align-self: center;
```