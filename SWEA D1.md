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



## 8) [2050. 알파벳을 숫자로 변환](https://swexpertacademy.com/main/code/problem/problemDetail.do?problemLevel=1&contestProbId=AV5QLGxKAzQDFAUq&categoryId=AV5QLGxKAzQDFAUq&categoryType=CODE&problemTitle=&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=1&pageSize=10&pageIndex=1)

```python
alp = input()
for i in alp:
    print(ord(i) - 64, end=' ')
```



## 9) [2047. 신문 헤드라인](https://swexpertacademy.com/main/code/problem/problemDetail.do?problemLevel=1&contestProbId=AV5QKsLaAy0DFAUq&categoryId=AV5QKsLaAy0DFAUq&categoryType=CODE&problemTitle=&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=1&pageSize=10&pageIndex=1)

```python
s_str = input()
print(s_str.upper(), end='')
```



## 10) [2046. 스탬프 찍기](https://swexpertacademy.com/main/code/problem/problemDetail.do?problemLevel=1&contestProbId=AV5QKdT6AyYDFAUq&categoryId=AV5QKdT6AyYDFAUq&categoryType=CODE&problemTitle=&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=1&pageSize=10&pageIndex=1)

```python
num = int(input())
print('#'*num)
```



## 11) [2043. 서랍의 비밀번호](https://swexpertacademy.com/main/code/problem/problemDetail.do?problemLevel=1&contestProbId=AV5QJ_8KAx8DFAUq&categoryId=AV5QJ_8KAx8DFAUq&categoryType=CODE&problemTitle=&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=1&pageSize=10&pageIndex=2)

```python
a, b = map(int, input().split())
print(a-b+1)
```



## 12) [2029. 몫과 나머지 출력하기](https://swexpertacademy.com/main/code/problem/problemDetail.do?problemLevel=1&contestProbId=AV5QGNvKAtEDFAUq&categoryId=AV5QGNvKAtEDFAUq&categoryType=CODE&problemTitle=&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=1&pageSize=10&pageIndex=2)

```python
T = int(input())
for test_case in range(1, T + 1):
	a, b = map(int, input().split())
	print(f'#{test_case} {a // b} {a % b}')
```



## 13) [2027. 대각선 출력하기](https://swexpertacademy.com/main/code/problem/problemDetail.do?problemLevel=1&contestProbId=AV5QFuZ6As0DFAUq&categoryId=AV5QFuZ6As0DFAUq&categoryType=CODE&problemTitle=&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=1&pageSize=10&pageIndex=2)

```python
for i in range(5):
    for j in range(5):
        if i == j:
            print('#', end='')
        else:
            print('+', end='')
    print()
```



## 14) [2025. N줄덧셈](https://swexpertacademy.com/main/code/problem/problemDetail.do?problemLevel=1&contestProbId=AV5QFZtaAscDFAUq&categoryId=AV5QFZtaAscDFAUq&categoryType=CODE&problemTitle=&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=1&pageSize=10&pageIndex=2)

```python
num = int(input())
result = 0
for i in range(1, num+1):
    result += i
print(result)
```



## 15) [1938. 아주 간단한 계산기](https://swexpertacademy.com/main/code/problem/problemDetail.do?problemLevel=1&contestProbId=AV5PjsYKAMIDFAUq&categoryId=AV5PjsYKAMIDFAUq&categoryType=CODE&problemTitle=&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=1&pageSize=10&pageIndex=2)

```python
a, b = map(int, input().split())
print(a+b)
print(a-b)
print(a*b)
print(a//b)
```



## 16) [1933. 간단한 N의 약수](https://swexpertacademy.com/main/code/problem/problemDetail.do?problemLevel=1&contestProbId=AV5PhcWaAKIDFAUq&categoryId=AV5PhcWaAKIDFAUq&categoryType=CODE&problemTitle=&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=1&pageSize=10&pageIndex=2)

```python
N = int(input())
for i in range(1, N + 1):
    if N % i == 0:
        print(i,end=' ')
```



## 17) [1936. 1대1 가위바위보](https://swexpertacademy.com/main/code/problem/problemDetail.do?problemLevel=1&contestProbId=AV5PjKXKALcDFAUq&categoryId=AV5PjKXKALcDFAUq&categoryType=CODE&problemTitle=&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=1&pageSize=10&pageIndex=2)

```python
a, b = map(int, input().split())
if (a - b) == -1 or (a - b) == 2:
    print('B')
elif (a - b) == -2 or (a - b) == 1:
    print('A')
```



## 18) [2019. 더블더블](https://swexpertacademy.com/main/code/problem/problemDetail.do?problemLevel=1&contestProbId=AV5QDEX6AqwDFAUq&categoryId=AV5QDEX6AqwDFAUq&categoryType=CODE&problemTitle=&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=1&pageSize=10&pageIndex=2)

```python
N = int(input())
for i in range(N+1):
    print(2**i, end=' ')
```



## 19) [1545. 거꾸로 출력해 보아요](https://swexpertacademy.com/main/code/problem/problemDetail.do?problemLevel=1&contestProbId=AV2gbY0qAAQBBAS0&categoryId=AV2gbY0qAAQBBAS0&categoryType=CODE&problemTitle=&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=1&pageSize=10&pageIndex=2)

```python
N = int(input())
for i in range(N+1):
    print(N-i, end=' ')
```

