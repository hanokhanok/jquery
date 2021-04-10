# 선택자
자식요소: children()
부모요소: parent(), parents(), closest()
다음요소: next(), nextAll(), nextUtil()
이전요소: prev(), prevAll(), prevUntil()
형제요소: siblings()

find() 하위요소 선택
filter() 조건에 맞는 요소를 걸러냄
not() ~이 아닌요소
has() ~을 포함하고 있는 요소
eq(n) index가 n인 요소
gt(n) index가 n보다 큰 요소
lt(n) index가 n보다 작은 요소

add() 요소를 더함
addBack() 이전 선택 요소를 더해서 선택
end() 실행이 끝나면 처음 선택자로 다시 돌아와서 실행
is() 선택한 요소를 판별해주는 선택자로 if문의 조건식에 사용됨

# 메서드

-배열-
$.each(배열명 또는 객체명, function(index, value) {

});
$(selector).each(function(index, value) {

});

$.map(배열명 또는 객체명, function(value, index) {

}); // map 메서드로 새로운 배열 생성 가능

-요소-
text(): 요소의 텍스트를 취득, 생성, 변경할 수 있음
html(): 선택한 요소의 자식 html을 취득, 생성, 변경할 수 있음
addClass(): 요소에 class 속성 추가
removeClass(): 요소의 class 속성 제거
toggleClass(): 요소에 class속성이 없으면 addClass()가 적용되고 있으면 removeClass()가 적용됨
hasClass(): 선택한 요소에 클래스가 있으면 true, 없으면 false를 반환

-css-
css()
width()
innerWidth() padding이 적용된 요소의 가로 길이를 취득, 변경
outerWidth() border와 margin이 적용된 요소의 가로 길이를 취득, 변경
height()
innerHeight() padding이 적용된 요소의 높이를 취득, 변경
outerHeight() border와 margin이 적용된 요소의 높이를 취득, 변경
offset() html 기준으로 left, top값을 취득, 변경
position() 부모 요소 기준으로 left, top값을 취득, 변경

-속성-
attr() 선택한 요소의 속성을 선택, 생성, 변경
prop() 자바스크립트의 property와 관련된 메서드. 요소의 속성을 true와 false로 제어함

-삽입-
prepend(), append(), before(), after()
prependTo(), appendTo(), insertBefore(), insertAfter()

-제거-
removeAttr() 요소의 속성 제거
empty() 하위요소 삭제
remove() 요소를 완전히 삭제
detach() 요소를 삭제하지만 필요할 때 원하는 위치에 다시 삽입할 수 있음 

-복사, 감싸기, 스크롤-
clone(), wrap(), wrapAll(), wrapInner(), replaceWith(), replaceAll()

scrollTop(), scrollLeft()

# jquery 이벤트
click(), dblclick(), mouseover(), mouseout(), mouseenter(), mouseleave(),
mousedown(), mouseup(), mousemove(), hover()

keydown(), keypress(), keyup()

ready(), resize(), scroll()

# jquery 효과
show(), hide(), toggle(), slideDown(), slideUp(), slideToggle(),
fadeIn(), fadeOut(), fadeTo(), fadeToggle()

$(selector).show(speed, easing, callback);
$(selector).hide(speed, easing, callback);
$(selector).toggle(speed, easing, callback);

# Custom 효과
animate() 메서드
$(selector).animate({속성: 값}, speed, easing, callback);

clearQueue() 현재 진행하고 있는 애니메이션까지는 진행이 되고 이후 애니메이션은 삭제

$(selector).stop(clearQueue, jumpToEnd) : 매개변수 기본값은 false

delay() 지정한 시간만큼 애니메이션을 지연시킴

# ajax 메서드
$.ajax({
  type: "GET", // 데이터를 읽어오는 방식
  url: "data.json", // 데이터 파일명
  dataType: "json", // 데이터 형식
  success: function(data) {
    // 로드에 성공 하였을 경우
  }
});