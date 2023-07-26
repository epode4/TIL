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

<br>

## 1. 변수 


**변수이름 = 값**

- 어떤 이름이든 사용 가능 
- 다만 영어, 숫자, _를 이용하여 선언
- 키워드는 사용 불가 

**Data type**

1. Number
2. Boolean
4. String

<br>

### 1-1. Number

| 숫자 | type | 타입 |
| :---: | :---: | :---: |
| 1 | int | 정수 |
| 1.1 | float | 소수 |
| 1-4j | complex | 복소수 |

<br>

### 1-2. Boolean

True, False로 이루어진 type
- `bool()`을 통해 확인

<br>

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

<br>

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


<br>

## 2. 연산자

1. 산술연산자
2. 비교연산자
3. 논리연산자
4. 복합연산자
5. 기타연산자

---
### 우선순위

0. ( )를 통해 그룹화
1. **
2. 산술연산자(*, /)
3. 산술연산자(+, -)
4. 비교연산자, in, is
5. not, and, or

<br>

### 2-1. 산술연산자

| 기호 | 의미 |
| :---: | :---: |
| + | 더하기 |
| - | 나누기 |
| * | 곱하기 |
| / | 나누기 |
| ** | 제곱 |
| // | 나눈 몫 |
| % | 나머지 값 |
| divmod() | 몫, 나머지 |

<br>

### 2-2. 비교연산자

연산자 왼쪽 값 기준

| 기호 | 의미 |
| :---: | :---: |
| > | 더 크다 |
| < | 더 작다 |
| >= | 크거나 같다 |
| <= | 작거나 같다 |
| == | 동일하다 |
| != | 동일하지 않다 |

- 연산자 왼쪽 값을 오른쪽 값과 비교한 결과로 `True`, `False`로 나옴
- `==` 는 문자도 비교 가능

<br>

### 2-3. 논리연산자

- `and` : 양쪽 모두 True일 때 `True` 출력
- `or` : 양쪽 모두 False일 때 `False`
- `not` : 반대값 반환

<br>
> 단축평가

`and` <br>
앞이 True : 뒷값 출력 <br>
앞이 False : 앞값 출력

`or`<br>
앞이 True : 앞값 출력 <br>
앞이 False : 뒷값 출력

<br>

### 2-4. 복합연산자

연산자 내용을 바로 적용하고 할당

| 일반연산자 | 복합연산자 |
| :---: | :---: |
| a = a + b | a += b |
| a = a - b | a -= b |
| a = a ** b | a **= b |

<br>

### 2-5. 기타연산자

- `+` (concatenation)
    - `a + b` 
    - 문자열, list 가능
- `in` (containment)
    - `'a' in 'apple'`, `1 in [1,2,3]`
    - True, False의 결과로 출력
- `is` (identify)
    - `a is b`
    - True, False의 결과로 출력

<br>

## 3. 형변환
    
1. 암시적 형변환
2. 명시적 형변환


### 3-1. 암시적 형변환

`True`, `False` 값이 숫자와 더해질 때 암시적으로 값이 변환됨
- `True` : 1
- `False` : 0


<br>

### 3-2. 명시적 형변환

- `int()` : string, float를 int로 변환
- `float()` : string, int를 float로 변화
- `str()` : int, float 등을 string으로 변환
- `bool()` : int, list 등을 boolean으로 변환

<br>

## 4. Sequence 자료형
데이터의 순서대로 나열된 자료구조 (정려될 것과는 다름)

1. List
2. Tuple
3. Range
4. String

<br>

### 4-1. List
- 선언 : 변수이름 = [value1, value2, value3]
- 접근 : 변수이름[index]
> 수정 가능 (mutable)

### 4-2. Tuple

- 선언 : 변수이름 = (value1, value2, value3)
- 접근 : 변수이름[index]

> 수정 불가능 (immutable)

### 4-3. Range
- range(n) : 0부터 n-1까지 범위
- range(n, m) : n부터 m-1까지 범위
- range(n, m, s) : n부터 m-1까지 +s만큼 증가하는 범위

### 4-4. String

기본 데이터 구조 참고

<br>

### 4-5. Sequence에서 활용 가능한 연산/함수

- `indexing[n]` : 원하는 자리의 값 뽑아내기
- `slicing[n:m]` : n부터  m전까지 뽑아내기
    - [n:m:k] : k 간격으로 n부터 m전까지 뽑아내기 
- `in` : 안에 있는지 확인하고 True, False 출력
    - `not in` : 없는지 확인
- `+` : 연결해서 붙이기
- `*` : 뒤에 오는 숫자만큼 연결하기
- `len` : 길이 출력
- `min` : 최솟값 출력
- `max` : 최댓값 출력
- `.count(n)` : n이 몇 번 들어가있는지 출력

<br>

## 5. Sequence가 아닌 자료구조

1. Set
2. Dictionary

<br>

### 5-1. Set
- 선언 : 변수이름 = {value1, value2, value3}

수학에서 사용하는 집합과 동일하게 처리(중복값 없음)



```python 
차집합
set_a - set_b

합집합 (중복값 제거)
set_a |set_b

교집합
set_a & set_b
```

<br>

### 5-2. Dictionary

- 선언 : 변수이름 = {key1: value1, key2: value2}

- 접근 : 변수이름[key]

- dictionary는 key와 value가 쌍으로 이루어져있다.

- key에는 immutable한 모든 것을 사용가능 (불변값 : string, integar)

- value에는 모든 데이터 가능 (list, dictionary도 가능)