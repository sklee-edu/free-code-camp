# Applied Visual Design
## text align
text-align: [left | right | center | justify]

## width, height
width: 20px;
height: 20px;
em : relative length units
px : absolute length units
percentage : parent element 기준

## text decoration
<strong> : bold
<em> : emphasize
<u> : underline
<s> : strikethrough
<hr> : horizontal line

## box-shadow
box-shadow: 0 10px 20px rgba(0,0,0,0.19), 0 6px 6px rgba(0,0,0,0.23);
x-offset, y-offset, [blur-radius, spread-radius], color

## opacity
1: opaque
0: transparent

## text-transform
transform me
lowercase: transform me
uppdercase: TRANSFORM ME
capitalize: Transform Me
initial : use the default value
inherit use the text-transform value from the parent element
none : use the original text

## font
color : 색상
font-size : 크기
font-weight : 굵기
font-family : 폰트
line-height : 한 줄 안에서의 간격

## pseudo-class
select specific state of the element
a:hover {
color: red;
}

## Position
Block-level items : start a new line ex. head, p, div
Inline items : surrounding content ex. img, span
normal flow : tag들이 default box model로 제공

position: static;
default 값
상하좌우 조절 불가능, normal-flow에 따라서만 위치

position: relative;
left: 20px;
상하좌우 조절 가능, normal-flow를 기준으로 얼마나 움직여야 하는지를 계산
다른 element의 normal-flow에는 큰 영향을 미치지 않는다
left와 같은 CSS offset property는 offset으로부터 20px 떨어지게 하는 것, 즉 오른쪽으로 20px 움직임

position: fixed;
viewport를 기준으로 fixed 되어 있음
페이지의 스크롤 등에 영향을 받지 않음

position: absolute;
relative to the nearest positioned ancestor
상하좌우 조절 가능, normal-flow를 무시
다른 element의 normal-flow에서 빠짐
원래 normal-flow를 무시하고, 가장 가까운 relative 부모를 기준으로 위치

## Float
Float element는 document의 normal flow에서 제거되고, element의 parent element를 기준으로 왼쪽 또는 오른쪽으로 이동한다. 
width와 함께 많이 이용

## z-index
overlapping 되었을 때 z-index를 줘서 해결

## center
margin: auto;
inline, block-level인지에 따라 다르게 작동 가능

## color
### RGB
primary : Red, Green, Blue
secondary : cyan (G + B), magenta (R + B) and yellow (R + G)
ternary : primary + secondary

complementary colors : opposite colors

### HSL
Hue, Saturation, Lightness
Hue : 색상에 해당, 0~360도로 표시
Saturation : 색상에 gray가 있는 양, 0~100%로 표시, 0%일 수록 회색이 많고, 100%일 수록 회색이 없음
Lightness : 흰색과 검정색의 양, 0(검정) ~ 100(흰색)%로 표시

### Linear Gradient
background: linear-gradient(gradient_direction, color 1, color 2, color 3, …);

background: repeating-linear-gradient(
45deg,
yellow 0px,
yellow 40px,
black 40px,
black 80px
);

## Background Image
background: url(https://i.imgur.com/MJAkxbh.png);

## Transform
### Scale
transform: scale(1.5);

### Skew
transform: skewX(24deg);
transform: skewY(-10deg);

## Pseudo-elements
::before, :: after
add something before or after a selected element

## Animation
#anim {
  animation-name: colorful;
  animation-duration: 3s;
  animation-fill-mode: forwards;
}
@keyframes colorful {
  0% {
    background-color: blue;
  }
  100% {
    background-color: yellow;
  }
}

animation-name : animation의 이름을 정의
animation-duration : animation의 기간을 정의
animation-fill-mode: animation이 종료된 다음에 어떻게 할지를 정의
animation-iteration-count: 몇 번 반복할 것인지 정의
animation-timinig-function : 애니메이션의 속도를 ease, linear 중 한 방식을 선택
@keyframes : 시간동안 무슨 일이 있을 것인지 정의

### Cubic-bazier
animation-timing-function: cubic-bezier(0.25, 0.25, 0.75, 0.75);
p0 : (0,0)
p1: (0.25, 0.25) 사용자가 지정
p2: (0.75, 0.75) 사용자 지정
p3: (1,1)
x축은 시간, y축은 변화의 정도