koreamapfont
============

한국 지도 글꼴을 사용하면 간단한 HTML과 CSS만으로 한국 지도를 그릴 수 있습니다.
주요 행정구역별로 색을 다르게 할 수 있어서 인포그래프에 도움이 됩니다.
미국 주별 지도 [Stately][Stately]를 보고 따라 [만들었습니다][making].
문자와 행정구역은 다음과 같이 대응했습니다.

[stately]: https://github.com/intridea/stately
[making]: https://github.com/intridea/stately/blob/master/MAKING.md

<table>
<tr><td rowspan="5">남한</td><td>강원도</td><td>a</td>
<td>경기도</td><td>b</td>
<td>경상남도</td><td>c</td>
<td>경상북도</td><td>d</td></tr>
<tr><td>광주광역시</td><td>e</td>
<td>대구광역시</td><td>f</td>
<td>대전광역시</td><td>g</td>
<td>부산광역시</td><td>h</td></tr>
<tr><td>서울특별시</td><td>i</td>
<td>세종특별자치시</td><td>j</td>
<td>울산관역시</td><td>k</td>
<td>인천광역시</td><td>l</td></tr>
<tr><td>전라남도</td><td>m</td>
<td>전라북도</td><td>n</td>
<td>제주특별자치도</td><td>o</td>
<td>충청남도</td><td>p</td></tr>
<tr><td>충청북도</td><td>q</td></tr>
<tr><td rowspan="3">북한</td><td>강원도</td><td>r</td>
<td>남포특별시</td><td>s</td>
<td>라선특별시</td><td>t</td>
<td>량강도</td><td>u</td></tr>
<tr><td>자강도</td><td>v</td>
<td>평안남도</td><td>w</td>
<td>평안북도</td><td>x</td>
<td>평양직할시</td><td>y</td></tr>
<tr><td>함경남도</td><td>z</td>
<td>함경북도</td><td>{</td>
<td>황해남도</td><td>|</td>
<td>황해북도</td><td>}</td></tr>
</table>

사용 방법
---------

글꼴과 CSS 파일을 [다운로드받고][download], 적절한 위치에 압축을 풉니다.
HTML `header`에 CSS 파일을 포함합니다.
글꼴 파일을 다른 위치로 이동했다면, CSS 파일 속 글꼴 경로를 수정합니다.

[download]: http://maczniak.github.com/koreamapfont/koreamapfont.zip

```html
<link rel="stylesheet" href="assets/css/korea-map-font-v1.css">
```

지도를 그릴 곳에 아래와 같이 추가합니다.
`class`는 행정구역별로 색을 지정하려고 넣었고, 필요하다면 값을 다르게 변경해도 됩니다.

```html
<ul class="korea-map-font-v1">
  <li class="강원">a</li>
  <li class="경기">b</li>
  <li class="경남">c</li>
  <li class="경북">d</li>
  <li class="광주">e</li>
  <li class="대구">f</li>
  <li class="대전">g</li>
  <li class="부산">h</li>
  <li class="서울">i</li>
  <li class="세종">j</li>
  <li class="울산">k</li>
  <li class="인천">l</li>
  <li class="전남">m</li>
  <li class="전북">n</li>
  <li class="제주">o</li>
  <li class="충남">p</li>
  <li class="충북">q</li>
</ul>
<!-- 북한 지도
<ul class="korea-map-font-v1">
  <li class="북강원">r</li>
  <li class="남포시">s</li>
  <li class="라선시">t</li>
  <li class="량강도">u</li>
  <li class="자강도">v</li>
  <li class="평안남">w</li>
  <li class="평안북">x</li>
  <li class="평양시">y</li>
  <li class="함경남">z</li>
  <li class="함경북">{</li>
  <li class="황해남">|</li>
  <li class="황해북">}</li>
</ul>
-->
```

지도의 크기와 기본 색을 지시합니다. 여기서 `width`와 `font-size`는 동일한 값으로 설정합니다.

```css
.korea-map-font-v1 {
  width: 300px;
  font-size: 300px;
  color: #f0f0f0;
}
```

행정구역별로 색을 다르게 합니다.

```css
.경기, .경북 {
  color: #FF0000;
}
```

아래 예제와 같이 한 페이지에 지도가 여러개 나온다면, 지도마다 `id`를 부여하여 서로 다른 크기와 색을 보여줄 수 있습니다.

예제
----

http://maczniak.github.com/koreamapfont/

참고
----

* Stately: https://github.com/intridea/stately
* GeoBats: http://www.dafont.com/font.php?file=geobats

TODO
----

* 멀리 떨어진 섬들을 다르게 보여주는 버전
* 다양한 크기에서 잘 보이도록 행정구역간 경계 다듬기

라이선스
--------

Creative Commons [Attribution-Share Alike 3.0 Unported][cc].

[cc]:http://creativecommons.org/licenses/by-sa/3.0/deed.en
