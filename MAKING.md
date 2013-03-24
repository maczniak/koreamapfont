지도 글꼴 만들기
================

기본적으로 [Stately][stately] 제작자가 쓴 [심볼 글꼴 만드는 방법][howto]과 동일합니다.
지도 원본은 [남한][south]과 [북한][north]입니다.
(기타 참고할 링크, [대한민국의 행정 구역][wikipedia] (위키백과), 세종특별자치시가 없는 지도 [1][map1], [2][map2])
잉크스케이프에서 아래 단계로 처리했습니다.

[stately]: https://github.com/intridea/stately
[howto]: http://www.intridea.com/blog/2012/4/24/symbol-font
[south]: http://en.wikipedia.org/wiki/File:South_Korea-Sejong.svg
[north]: http://ko.wikipedia.org/wiki/%ED%8C%8C%EC%9D%BC:Divisions_of_North_Korea_ko.svg
[wikipedia]: http://ko.wikipedia.org/wiki/%EB%8C%80%ED%95%9C%EB%AF%BC%EA%B5%AD%EC%9D%98_%ED%96%89%EC%A0%95_%EA%B5%AC%EC%97%AD
[map1]: http://commons.wikimedia.org/wiki/File:Provinces_of_South_Korea.svg
[map2]: http://ko.wikipedia.org/wiki/%ED%8C%8C%EC%9D%BC:Gyeonggi_Localmap.svg

* Object > Ungroup - Path로 변환하기위해 섬들을 분리
* Path > Object to Path - 선택을 Path로 변환
* Path > Union - 다시 내륙과 섬들을 묶음
* Path > Simplify - Edit > XML Editor...로 보기에 `<svg:path>`의 `style` 속성에 `transform()`이 있는 경우
  글꼴로 변환했을 때 위치가 이상해지는 현상 방지

내륙에 빈 공간이 생기지 않도록 Font Squirrel에서 OPTIMAL 대신 BASIC 옵션을 사용합니다.