#Applied Accessibility
## Alt image
<img src=“something” alt=“alt” />
img가 단순한 decoration일 때는 alt를 입력해줄 필요가 없음

## Heading(h1 ~ h6)
Hierarchical Relationships of Content

## Content using the main content
main, header, footer, nav, article, and section
div와 비슷한 역할을 함

### main 
한 페이지에 하나만 있음
핵심적인 역할을 함

### article
<div> - groups content 
<section> - groups related content
<article> - groups independent, self-contained content

ex. book is <article>, chapter is <section>

### header
introductory information or navigation links
<head>와 다름

### nav
navigation이 있다면, nav로 바꿀 필요가 있음

### footer
밑에 나오는 부분

### audio
<audio id="meowClip" controls>
  <source src="audio/meow.mp3" type="audio/mpeg" />
  <source src="audio/meow.ogg" type="audio/ogg" />
</audio>

### figure, fig caption
<figure>
  <img src="roundhouseDestruction.jpeg" alt="Photo of Camper Cat executing a roundhouse kick">
  <br>
  <figcaption>
    Master Camper Cat demonstrates proper form of a roundhouse kick.
  </figcaption>
</figure>


### label
form field에서 선택지에 더 의미를 부여하기 위해서

<form>
  <label for="name">Name:</label>
  <input type="text" id="name" name="name">
</form>

<form>
  <label>
    Name:
    <input type=“text” name=“name />
  </label>
</form>

### fields, legendary
Radio button 중에 선택할 때 더 잘 선택하기 위해
<form>
  <fieldset>
    <legend>Choose one of these three items:</legend>
    <input id="one" type="radio" name="items" value="one">
    <label for="one">Choice One</label><br>
    <input id="two" type="radio" name="items" value="two">
    <label for="two">Choice Two</label><br>
    <input id="three" type="radio" name="items" value="three">
    <label for="three">Choice Three</label>
  </fieldset>
</form>

### date picker
input에서 date도 받을 수 있음
<label for="input1">Enter a date:</label>
<input type="date" id="input1" name="input1”>


### Time
시간을 나타내는 태그인 <time>과 attribute인 datetime이 추가
<p>Master Camper Cat officiated the cage match between Goro and Scorpion <time datetime="2013-02-13">last Wednesday</time>, which ended in a draw.</p>

### Screen Read Only
Screen Read에서 읽기 위해서는 보이기는 해야하기 때문에 0px로 설정 해두면 안 된다
.sr-only {
  position: absolute;
  left: -10000px;
  width: 1px;
  height: 1px;
  top: auto;
  overflow: hidden;
}

### access key
accesskey를 이용해 단축키롤 접근 가능
<button accesskey="b">Important Button</button>

### tab index
tabindex를 통해 tab을 통해 변경 가능
<div tabindex="0">I need keyboard focus!</div>