기본적으로 console은 테스트를 위해 제작되었기 때문에 console에서 특정행위들을 할때 return 값을 보여주게 되어있습니다.
calcRectArea는 return 값이 존재하는 함수이기에 return을 보여주고
console.log함수는 return 값이 존재하지 않는 함수이기에 undefined가 반환됩니다.

console.log는 괄호 안의 값을 로깅해주는 함수이기 때문에 들어간 함수인 calcRectArea(4, 3)이 리턴해준 값인 12를 로깅하고 그 뒤에는 console 단위에서 console.log 라는 함수 값의 return 값을 보여주는 것인데 console.log 함수는 위에서 서술하였듯이 return 값이 존재하지 않는 함수이기 때문에 undefined가 console에 찍히게 됩니다.

앞에 작게 ( < ) 회색 화살표가 붙어있는 부분이 console에서 자동적으로 return 값을 보여주는 부분입니다.
그래서 console.log에서 undefined가 나오는 부분 앞에는 작게 화살표 ( < )가 붙어있습니다.

### 예)
```javascript
function calcRectArea(width, height) {
 return width * height;
}

< undefined // console이 함수의 선언이라는 행위에는 return 값이 존재하지 않기 때문에 undefined 출력

calcRectArea(4,3)

< 12 // console이 calcRectArea 함수 호출시 인자 4와 3이라는 두 인자를 이용해 계산해서 나온 결과값인 12를 반환하기에 12 출력

console.log(calcRectArea(3,4))

12 // console.log 가 calRectArea의 return 값인 12를 출력

< undefined // console이 console.log 는 return 값이 존재하기 않기 때문에 undefined 출력
```
