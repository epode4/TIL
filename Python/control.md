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
