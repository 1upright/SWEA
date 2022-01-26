# SWEA D2

## 1) [1859. 백만 장자 프로젝트](https://swexpertacademy.com/main/code/problem/problemDetail.do?problemLevel=2&contestProbId=AV5LrsUaDxcDFAXc&categoryId=AV5LrsUaDxcDFAXc&categoryType=CODE&problemTitle=&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=2&pageSize=10&pageIndex=1&&&&&&&&&&)

```python
T = int(input())
for test_case in range(1, T + 1):
    N = int(input())
    bargain = list(map(int, input().split()))
    result = 0
    last_price = bargain[N - 1]
    for i in range(N - 1, -1, -1):
        if bargain[i] <= last_price:
            result = result + last_price - bargain[i]
        else:
            last_price = bargain[i]
    print(f'#{test_case} {result}')
```



## 2) [1926. 간단한 369게임](https://swexpertacademy.com/main/code/problem/problemDetail.do?problemLevel=2&contestProbId=AV5PTeo6AHUDFAUq&categoryId=AV5PTeo6AHUDFAUq&categoryType=CODE&problemTitle=&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=2&pageSize=10&pageIndex=1)

```python
N = int(input())
for i in range(1, N + 1):
    score = str(i).count('3') + str(i).count('6') + str(i).count('9')
    if score:
        print('-' * score, end=' ')
    else:
        print(i, end=' ')
```



```python
# 인터넷에서 본 다른 풀이
N = int(input())
clap = ['3', '6', '9']

for i in range(1, N+1):
    count = 0
    for j in str(i):
        if j in clap:
            count += 1
    if count > 0:
        i = '-' * count
    print(i, end=' ')
```



## 3) [2007. 패턴 마디의 길이](https://swexpertacademy.com/main/code/problem/problemDetail.do?problemLevel=2&contestProbId=AV5P1kNKAl8DFAUq&categoryId=AV5P1kNKAl8DFAUq&categoryType=CODE&problemTitle=&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=2&pageSize=10&pageIndex=1)

```python
T = int(input())
for test_case in range(1, T + 1):
    word = input()
    for i in range(1, 10):
        if word[:i] == word[i:2*i]:
            print(f'#{test_case} {i}')
            break
```

