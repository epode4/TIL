# 제어문

1. 조건문 

<br>

## 1. 조건문 (if문)

1. if문을 반드시 일정한 참/거짓을 판단할 수 있는 **조건식**과 함께 사용한다. 

2. <br> 조건식이 참인 경우 `:` 이후 문장 실행 <br>
조건식이 거짓인 경우 `else:` 이후 문장 실행


### if-else문
```python
if <조건식>:
    if의 조건이 참인 경우 실행
else:
    if의 조건이 거짓인 경우 실행

```

<br>

 ### elif문

 여러 조건을 사용할 수 있는 조건문

 ```python
 if <조건식>:
    if의 조건이 참인 경우 실행
elif <조건식>:
    elif의 조건이 참인 경우 실행
...
else:
    위의 조건식이 하나도 부합하지 않는 경우 실행
 ```

 <br>

### 조건표현식

```python
true_value if <조건식> else false_value
```
**동일한 코드**

```python
if <조건식>:
    true_value
else:
    false_value
```

<br>

## 반복문
<br>

### while문
표현식이 참인 동안 실행을 반복

```python
while <조건식>:
    실행할 코드
```
<br>

### for문
정해진 범위 내에서 반복을 실행

```python
for variable in sequence:
    code
```

- variable : 단수
- sequence : 복수
 
> 주로 for문을 사용해 사용자가 입력한 데이터를 한글자씩 출력

<br>

### dictionary 반복

```python
1. for key in dict
    - key 출력

2. for key in dict.keys()
    - 1과 동일하나 좀 더 명시적

3. for value in dict.values()
    - value 출력

4. for key, value in dict.items()
    - key와 value 모두 출력
```

<br>

### break
break를 사용하여 반복문을 종료

---
### continue
continue 이후의 코드를 실행하지 않고 다음 반복을 진행

---
### else (for - else)
반복문이 끝까지 진행되어야 실행 가능

---
### pass
구조적으로 문장이 필요할 때 잠시 사용하는 아무 의미 없는 문장

## match

값이 일치하는 경우 해당 case문을 실행

```python
match value
    case <조건>:
        code
    case <조건>:
        code
    case _:
        code
```

