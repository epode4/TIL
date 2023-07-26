# Python_jupyter notebook 사용법

## 단축키

- ctrl + enter : 현재 cell 실행
- shift + enter : 현재 cell 실행 + 다음 cell로 이동
- alt + enter : 현재 cell 실행 + 새로운 cell 추가
- enter : insert 상태 실행
- esc : insert 상태에서 벗어나기
    - m : markdown으로 변환
    - y : code로 변환
    - x : cell 삭제 

## 주의사항

1. 대소문자 구분
2. 띄어쓰기 구분
3. 철자 확인

## 1. 변수 

```
변수이름 = 값
```
- 어떤 이름이든 사용 가능 
- 다만 영어, 숫자, _를 이용하여 선언
- 키워드는 사용 불가 

**Data type**

1. Number
2. Boolean
4. String

### 1-1. Number

| 숫자 | type | 타입 |
| :---: | :---: | :---: |
| 1 | int | 정수 |
| 1.1 | float | 소수 |
| 1-4j | complex | 복소수 |

### 1-2. Boolean

True, False로 이루어진 type
- `bool()`을 통해 확인

### 1-3. String
`'`, `"` 을 사용해서 표현
- 둘 중에 무엇을 사용하든 상관없지만 일관되게 사용
- 숫자를 넣어도 문자열로 인식

> 문자열 안에 따옴표를 사용하고 싶을 때 
1. `'`, `"` 같이 사용해서 구분
2. `\'` 로 문자열에 사용되는 따옴표라는 것을 알리기 

> 문자열 내에서 여러 줄 작성하기
1. ` ``` ``` ` 안에서 문자열을 작성하기
2. `\n` 으로 다음줄로 이동하기 (`\t`는 tab)

**String interpolation**
1. %-formatting
2. str.format()
3. f-string



```
age = 20
1. ('홍길동은 %s 살', %age)

2. ('홍길동은 {}살', .format(age))

3. (f'홍길동은 {age}살')
```

