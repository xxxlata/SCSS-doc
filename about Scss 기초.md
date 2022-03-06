## scss

styles -> css로 컴파일함
css preprocessor

scss는 css를 프로그래밍 랭귀지처럼 만들어줌
sytax를 개선하고 variables funtions..등등 사용가능
개발 속도가 빨라짐
오류를 바로 알려주기 때문에 오류수정에 용이함
코드 가독성이 좋다.

-----------------------------------------------------------------
gulp?
compile 하거나 transform 해주는 nodeJS package이다.

설정이 끝나고 npm i (npm install 해주는것)
 npm run dev 또는 yarn dev로 실행해준다

gulp 파일에 있는 (src주소파일) 모든일은 css로 compile된다.

------------------------------------------------------------------
variables<br><br>

$표시로 varialbles를 만들수있다. 
따로 scss파일을 만들어서 varialbles를 넣고
기존 scss파일에 ```@import "_variables";```
파일을 임포트 해주면 연결된다.

-----------------------------------------------------------------
nesting

```
ex) 
.box {
  margin-top: 20px;
  &:hover {
    background-color: green;  //기본은 .box:hover{}
  }
  h2 {
    color:blue;
  }
  button {
    color:red;
  }
}
```
box에 액션을 주고싶다면 &를 사용하여 추가할 수 있다.
이런식으로 부모 컨테이너 안에 직접 넣어서 자식 컨테이너를 설정할 수 있다.

--------------------------------------------------------------------
@mixin<br><br>

프로그램 로직을 짤 수 있다.
```
ex) 
@mixin link($word) {
  text-decoration: none;
  display: block;
  @if $word == "odd" {
    color:blue;
  } @else {
    color: red;
  }
}
```

--------------------------------------------------------------------
extends

말그대로 다른 코드를 확장(extend)하거나 코드를 재사용하고 싶을 때 사용 할 수 있다. 
