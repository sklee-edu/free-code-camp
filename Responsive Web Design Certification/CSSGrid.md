# CSS Grid

# For container(parent)
## CSS Grid
parent는 container, child는 element라고 불림
```css
display: grid;
```

## grid-template-columns && grid-template-rows
parent에 grid의 structure를 정의해야함
grid-template-columns를 통해 column의 갯수와 크기를 정함
grid-template-rows를 통해 row의 갯수와 크기를 정함
```css
.container {
  display: grid;
  grid-template-columns: 50px 50px;
  grid-template-rows: 5px 5px;
}
```

## size
auto는 content의 사이즈만큼 커짐
50px는 50px 크기
10%는 전체 container의 10%
2fr, 1fr은 남은 크기를 2:1로 나눔
```css
grid-template-columns: auto 50px 10% 2fr 1fr; 
```

## gap
column, row 사이에 gap을 줌
```css
grid-column-gap: 10px;
grid-row-gap: 5px;
grid-gap: 5px 10px;
```

# For child(element)
## grid-column & grid-row
element들을 column, row라고 하고 그 양 옆으로 있는 것들을 lines(grid)라고 함
어떤 column을 사용할지 lines를 기준으로 설정해줌
multiple column또는 다른 시작점을 가질 수 있다는 장점이 있음
```css
grid-column: 1 / 3;
grid-row: 2 / 4;
```

## justify-self
content가 cell을 horizontal하게 채우는 방법에 대해서 정의함
stretch가 default 값임
parent container에서 justify-items를 통해 일괄적으로 조절도 가능
```css
justify-self: [start, center, end, stretch];
```

## align-self
content가 cell을 vertical하게 채우는 방법에 대해서 정의함
parent container에서 align-items를 통해 일괄적으로 조절도 가능
```css
align-self: [start, center, end, stretch];
```

## grid-template-areas
parent에서 cell들을 group으로 만들고 이름을 줄 수 있음
띄어쓰기 단위로 cell이 구분 되고, ""단위로 row가 구분이 되고, .를 이용해 empty cell을 표현함
```css
grid-template-areas:
  "header header header"
  "advert content content"
  "footer footer footer";
```

## grid-area
child에서 cell듩을 template에서 지정한 이름에 위치하게 만듬
또는 line을 통해서 지정할 수도 있음
```css
.item1 { grid-area: header; }

.item1 { grid-area: 1/1/2/4; }
grid-area: horizontal line to start at / vertical line to start at / horizontal line to end at / vertical line to end at;
```

## repeat
repeat을 이용해서 반복되는 코드 양을 줄일 수 있음
```css
grid-template-rows: repeat(n, a);
a를 n번만큼 반복해서 입력함

grid-template-rows: repeat(100, 50px);
```