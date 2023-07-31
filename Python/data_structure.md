# Method

객체와 연관되어 있는 함수 

```python 
object.method() 
```
<br>

# 1. String method

String : immtable 하기에 원본 데이터는 수정되지 않음
```python
a = 'hi hello'
b = a.title(a)
print(b)
```
---

### `''.join(iterable)`
iterable한 객체를 ' ' 안 구분자를 사용해 붙인 뒤 하나의 문자열로 출력

---
### `replace(old, new[,count])`
string 속 old 문자를 new 문자로 변환(count를 통해 개수 지정 가능)

---
### `.strip([chars])`
chars에서 원하는 문자나 공백 제거

---
### `.find(x)`
string에서 원하는 문자의 index 출력
(중복일 경우 첫번째만 출력)

---
### `.index(x)`

string에서 원하는 문자의 index 출력

> `.find()`와 `.index()`의 차이점 : string 에 없는 값을 입력하면 `.find()` 는 -1의 음수 값 출력 / `.index()` 는 에러 발생

---
### `.split()`
구분자를 사용하여 string을 분할한 뒤 list로 저장

---
### `.count(x)`
string 속 원하는 문자의 개수 출력

<br>

# 2. List Method

List : mutable 하기에 원본 데이터가 변환
```python
a = [1, 2, 3, 4, 5]
a.remove(3)
print(a)
```

---
### `.append(x)`
원하는 요소를 list 마지막에 추가

---
### `.extend(iterable)`
원하는 list를 list 마지막에 추가(list + list 와 동일함)

---
### `.insert(idx,x)`
지정한 index 자리에 원하는 요소 추가

---
### `.remove(x)`
원하는 요소를 list 에서 제거

---
### `.pop([idx])`
index 값을 입력하면 해당 위치의 요소 삭제, 입력값이 없으면 맨 뒤의 값부터 삭제

---
### `.sort([reverse = True])`
list 값을 오름차순으로 정렬, 내림차순을 원할 시 옵션 입력

---
### `.reverse()`
list를 역순으로 변환

<br>

## 2.1 List copy

 `=` 를 사용하여 복사본을 만들 경우 해당 복사본의 요소가 변화하면 원본의 요소도 변환

 ```python
 a = [1, 2, 3]
 b = a

 b[0] = 100
 print(a)
 [100, 2, 3]
 ```

 ### 1. slicing으로 copy

 ```python
a = [1, 2, 3]
b = a[:]
 ```

 ### 2. list()로 copy
 ```python
 a = [1, 2, 3]
 b = list(a)
 ```

 ### 3. import copy 후 deepcopy

 만약 list 내 list 가 있을 경우 deepcopy 필요

 ```python
 import copy
 a = [1, 2, [3, 4]]
 b = copy.deepcopy(a)
 ```

 <br>

 ## 2.2 List Comprehension
 > comprehension : 객체를 쉽게 한 문장으로 생성하기 위해 사용 

 ```python
for문 사용

 my_list = []
 for i in numbers:
    if i == n:
        my_list.append(i) 
 ```
<br>

 ```python
 comprehension

my_list = [i for i in numbers if i == n]
 
 ```

 <br>

 # 3. Dictionary Method
Dictionary : mutable


### `.pop(key[, default])`
해당하는 key와 value 같이 삭제, 해당값이 없는 경우 default 값 출력

---
### `.update(key = value)`

해당하는 key의 value 입력한 값으로 바꾸기

---
### `.get(key[, default])`

해당하는 key의 value 값 출력, 해당값이 없는 경우 default 값 출력

<br>

## 3.1 Dictionary Comprehension

```python
for문

result = []
for k,v in dict.items():
    if v > n:
        result[k] = v
```
<br>

```python
comprehension

result = [k:v for k,v in dict.items() if v > n]
```

<br>

# 4. Set Method
method가 작동(추가, 삭제)하는 위치가 랜덤

### `.add(x)`
원하는 요소 set에 추가(중복된 데이터는 추가되지 않음)

---
### `.update({x, y})`
원하는 요소 set에 추가, 단어만 넣을 경우 단어 속 철자별로 추가되기에 set 형식으로 추가해야 함

---

### `.remove(x)`

원하는 요소 set에서 삭제

---
### `.pop()`
랜덤한 요소 set에서 삭제

<br>

# 5. map(), zip(), filter()

 세 함수 모두 list()를 사용해서 list로 변환한 뒤 출력해야 함

## 5.1 map()

iterable 객체의 요소들을 지정된 function으로 처리

`map(funciton, iterable)`

```python
a = [1, 2, 3]
b = map(str, a)
print(list(b))
b = ['1', '2', '3']
```

<br>

## 5.2 zip()
개수가 동일한 2개의 list를 묶어줌

`zip(list_1, list_2)`

```python
a = [1, 2, 3]
b = [100, 200, 300]

c = zip(a, b)
print(list(c))
c = [(1, 100), (2, 200), (3, 300)]
```

<br>

## 5.3 filter()

특정 조건을 충족하여 True 값을 보이는 요소만 추출

`filter(function, iterable)`
- function의 return 값이 무조건 True/False 이어야 함

```python
a = [1, 2, 3, 4, 5]
b = filter(function, a)

print(list(b))
b = [1, 3, 5]
```