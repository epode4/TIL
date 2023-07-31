#  1. 모듈(Module)

python 정의와 문장들을 담고 있는 파일(py 확장자)

- `import module_name`
- `module_name.function_name()`으로 모듈 내 함수 실행

<br>

# 2. 패키지(Package)
module의 집합
```python
myPackage/
    __init__.py
    math/
        __init__.py
        fibo.py
        formula.py
```
패키지 안에 `__init__.py` 파일이 있어야 패키지로 인식
<br>

- 패키지 폴더 전체 추가
```python
import package_name
```
<br>

- 패키지에서 원하는 모듈 꺼내오기
```python
from package.package import module [as name]
```
> as 붙여서 원하는 이름으로 불러오기 가능


<br>
- 경로에 있는 모듈이 가지고 있는 모든 변수, 함수 추가

```python
from package.package.module import *
```

<br>

# 3. Python 내장 패키지

`import package_name`으로 불러온 뒤 실행

## 3.1 math
수학 함수를 제공하는 패키지

- `math.ceil()` : 올림 함수
- `math.floor()` : 내림 함수
- `math.sqrt()` : 제곱근 함수

<br>

## 3.2 random
난수 생성 패키지

- `random.random()` : 0 ~ 1 사이 랜덤한 소수 출력
- `random.randint(n,m)` : n과 m사이 랜덤한 정수 출력
- `random.seed(n)` : 고정된 난수 생성 위한 seed 고정
- `random.choice()` : sequence 객체에서 랜덤한 요소 선택
- `random.sample()` : 비복원추출을 활용한 난수 생성

<br>

## 3.2 datetime

날짜와 시간 관련 패키지
`from datetime import`

- `datetime.now()` & `datetime.today()` : 현재 지역 날짜와 시간 출력
- `datetime.utcnow()` : 현재 UTC 기준 날짜와 시간 출력
- `now.strftime('%Y년 %m월 %d일')` : 현재 년, 월, 일을 문자열 형식으로 출력
- `now.year` & `now.day` : 현재 년, 일 출력
- `now.weekday()` : 0 ~ 6의 인덱스로 현재 요일 출력
- `timedelta()` : 특정 시간 저장(연산 가능)
- `datetime(Y, M, D)` : 날짜 저장(연산 가능)
