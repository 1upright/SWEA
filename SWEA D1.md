# SWEA D1



## 1) [2072. 홀수만 더하기](https://swexpertacademy.com/main/code/problem/problemDetail.do?problemLevel=1&contestProbId=AV5QSEhaA5sDFAUq&categoryId=AV5QSEhaA5sDFAUq&categoryType=CODE&problemTitle=&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=1&pageSize=10&pageIndex=1)

```python
T = int(input())
for test_case in range(1, T+1):
    numbers = list(map(int, input().split()))
    sum = 0
    for i in numbers:
        if i % 2 == 1:
            sum += i
    print(f'#{test_case} {sum}')
```



## 2) [2071. 평균값 구하기](https://swexpertacademy.com/main/code/problem/problemDetail.do?problemLevel=1&contestProbId=AV5QRnJqA5cDFAUq&categoryId=AV5QRnJqA5cDFAUq&categoryType=CODE&problemTitle=&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=1&pageSize=10&pageIndex=1)

```python
T = int(input())
for test_case in range(1, T+1):
    numbers = list(map(int, input().split()))
    num_av = round(sum(numbers) / len(numbers))
    print(f'#{test_case} {num_av}')
```



## 3) [2070. 큰 놈, 작은 놈, 같은 놈](https://swexpertacademy.com/main/code/problem/problemDetail.do?problemLevel=1&contestProbId=AV5QQ6qqA40DFAUq&categoryId=AV5QQ6qqA40DFAUq&categoryType=CODE&problemTitle=&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=1&pageSize=10&pageIndex=1)

```python
T = int(input())
for test_case in range(1, T+1):
    numbers = list(map(int, input().split()))
    if numbers[0] > numbers[1]:
        result = '>'
    elif numbers[0] < numbers[1]:
        result = '<'
    else:
        result = '=' 
    print(f'#{test_case} {result}')
```



##  4) [2068. 최대수 구하기](https://swexpertacademy.com/main/code/problem/problemDetail.do?problemLevel=1&contestProbId=AV5QQhbqA4QDFAUq&categoryId=AV5QQhbqA4QDFAUq&categoryType=CODE&problemTitle=&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=1&pageSize=10&pageIndex=1)

```python
T = int(input())
for test_case in range(1, T+1):
    numbers = list(map(int, input().split()))
    result = max(numbers)
    print(f'#{test_case} {result}')
```

```python
T = int(input())
for test_case in range(1, T+1):
    numbers = list(map(int, input().split()))
    maxvalue = numbers[0]
    for i in numbers:
        if i > maxvalue:
            maxvalue = i
    print(f'#{test_case} {maxvalue}')
```





## 5) [2063. 중간값 찾기](https://swexpertacademy.com/main/code/problem/problemDetail.do?problemLevel=1&contestProbId=AV5QPsXKA2UDFAUq&categoryId=AV5QPsXKA2UDFAUq&categoryType=CODE&problemTitle=&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=1&pageSize=10&pageIndex=1)

```python
N = int(input())
numbers = list(map(int, input().split()))
numbers.sort()
print(numbers[(N-1) // 2])
```



## 6) [2058. 자릿수 더하기](https://swexpertacademy.com/main/code/problem/problemDetail.do?problemLevel=1&contestProbId=AV5QPRjqA10DFAUq&categoryId=AV5QPRjqA10DFAUq&categoryType=CODE&problemTitle=&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=1&pageSize=10&pageIndex=1)

```python
N = int(input())
result = 0
for i in str(N):
    result += int(i)
print(result)
```



## 7) [2056. 연월일 달력](https://swexpertacademy.com/main/code/problem/problemDetail.do?problemLevel=1&contestProbId=AV5QLkdKAz4DFAUq&categoryId=AV5QLkdKAz4DFAUq&categoryType=CODE&problemTitle=&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=1&pageSize=10&pageIndex=1)

```python
T = int(input())
for test_case in range(1, T+1):
    number = input()
    year = int(number[:4])
    month = int(number[4:6])
    date = int(number[6:])

    if month < 1 or month > 12:
        print(f'#{test_case} -1')
        continue
    
    elif month == 2:
        if date < 1 or date > 28:
            print(f'#{test_case} -1')
            continue
    
    elif month in [4, 6, 9, 11]:
        if date < 1 or date > 30:
            print(f'#{test_case} -1')
            continue
    
    else:
        if date <1 or date > 31:
            print(f'#{test_case} -1')
            continue
    
    print('#%d %04d/%02d/%02d' %(test_case, year, month, date))
```

