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
    for i in range(1, 11):
        if word[:i] == word[i:2*i]:
            print(f'#{test_case} {i}')
            break
```



## 4) [2005. 파스칼의 삼각형](https://swexpertacademy.com/main/code/problem/problemDetail.do?problemLevel=2&contestProbId=AV5P0-h6Ak4DFAUq&categoryId=AV5P0-h6Ak4DFAUq&categoryType=CODE&problemTitle=&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=2&pageSize=10&pageIndex=1)

```python
```



## 5) [2001. 파리 퇴치](https://swexpertacademy.com/main/code/problem/problemDetail.do?problemLevel=2&contestProbId=AV5PzOCKAigDFAUq&categoryId=AV5PzOCKAigDFAUq&categoryType=CODE&problemTitle=&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=2&pageSize=10&pageIndex=1)
```python
```



## 6) [1989. 초심자의 회문 검사](https://swexpertacademy.com/main/code/problem/problemDetail.do?problemLevel=2&contestProbId=AV5PyTLqAf4DFAUq&categoryId=AV5PyTLqAf4DFAUq&categoryType=CODE&problemTitle=&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=2&pageSize=10&pageIndex=1)
```python
```



## 7) [1986. 지그재그 숫자](https://swexpertacademy.com/main/code/problem/problemDetail.do?problemLevel=2&contestProbId=AV5PxmBqAe8DFAUq&categoryId=AV5PxmBqAe8DFAUq&categoryType=CODE&problemTitle=&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=2&pageSize=10&pageIndex=1)

```python
```



## 8) [1984. 중간 평균값 구하기](https://swexpertacademy.com/main/code/problem/problemDetail.do?problemLevel=2&contestProbId=AV5Pw_-KAdcDFAUq&categoryId=AV5Pw_-KAdcDFAUq&categoryType=CODE&problemTitle=&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=2&pageSize=10&pageIndex=1)
```python
```



## 9) [1983. 조교의 성적 매기기](https://swexpertacademy.com/main/code/problem/problemDetail.do?problemLevel=2&contestProbId=AV5PwGK6AcIDFAUq&categoryId=AV5PwGK6AcIDFAUq&categoryType=CODE&problemTitle=&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=2&pageSize=10&pageIndex=1)

```python
```



## 10) [어디에 단어가 들어갈 수 있을까](https://swexpertacademy.com/main/code/problem/problemDetail.do?problemLevel=2&contestProbId=AV5PuPq6AaQDFAUq&categoryId=AV5PuPq6AaQDFAUq&categoryType=CODE&problemTitle=&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=2&pageSize=10&pageIndex=1)

```python
```



## 11) [1976. 시각 덧셈](https://swexpertacademy.com/main/code/problem/problemDetail.do?problemLevel=2&contestProbId=AV5PttaaAZIDFAUq&categoryId=AV5PttaaAZIDFAUq&categoryType=CODE&problemTitle=&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=2&pageSize=10&pageIndex=2)
```python
```



## 12) [1974. 스도쿠 검증](https://swexpertacademy.com/main/code/problem/problemDetail.do?problemLevel=2&contestProbId=AV5Psz16AYEDFAUq&categoryId=AV5Psz16AYEDFAUq&categoryType=CODE&problemTitle=&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=2&pageSize=10&pageIndex=2)
```python
```



## 13) [1970. 쉬운 거스름돈](https://swexpertacademy.com/main/code/problem/problemDetail.do?problemLevel=2&contestProbId=AV5PsIl6AXIDFAUq&categoryId=AV5PsIl6AXIDFAUq&categoryType=CODE&problemTitle=&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=2&pageSize=10&pageIndex=2)
```python
```



## 14) [1966. 숫자를 정렬하자](https://swexpertacademy.com/main/code/problem/problemDetail.do?problemLevel=2&contestProbId=AV5PrmyKAWEDFAUq&categoryId=AV5PrmyKAWEDFAUq&categoryType=CODE&problemTitle=&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=2&pageSize=10&pageIndex=2)
```python
```



## 15) [1961. 숫자 배열 회전](https://swexpertacademy.com/main/code/problem/problemDetail.do?problemLevel=2&contestProbId=AV5Pq-OKAVYDFAUq&categoryId=AV5Pq-OKAVYDFAUq&categoryType=CODE&problemTitle=&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=2&pageSize=10&pageIndex=2)
```python
```



## 16) [1959. 두 개의 숫자열](https://swexpertacademy.com/main/code/problem/problemDetail.do?problemLevel=2&contestProbId=AV5PpoFaAS4DFAUq&categoryId=AV5PpoFaAS4DFAUq&categoryType=CODE&problemTitle=&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=2&pageSize=10&pageIndex=2)
```python
```



## 17) [1954. 달팽이 숫자](https://swexpertacademy.com/main/code/problem/problemDetail.do?problemLevel=2&contestProbId=AV5PobmqAPoDFAUq&categoryId=AV5PobmqAPoDFAUq&categoryType=CODE&problemTitle=&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=2&pageSize=10&pageIndex=2)
```python
```



## 18) [1948. 날짜 계산기](https://swexpertacademy.com/main/code/problem/problemDetail.do?problemLevel=2&contestProbId=AV5PnnU6AOsDFAUq&categoryId=AV5PnnU6AOsDFAUq&categoryType=CODE&problemTitle=&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=2&pageSize=10&pageIndex=2)
```python
```



## 19) [1946. 간단한 압축 풀기](https://swexpertacademy.com/main/code/problem/problemDetail.do?problemLevel=2&contestProbId=AV5PmkDKAOMDFAUq&categoryId=AV5PmkDKAOMDFAUq&categoryType=CODE&problemTitle=&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=2&pageSize=10&pageIndex=2)
```python
```



## 20) [1945. 간단한 소인수분해](https://swexpertacademy.com/main/code/problem/problemDetail.do?problemLevel=2&contestProbId=AV5Pl0Q6ANQDFAUq&categoryId=AV5Pl0Q6ANQDFAUq&categoryType=CODE&problemTitle=&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=2&pageSize=10&pageIndex=2)
```python
```



## 21) [1940. 가랏! RC카!](https://swexpertacademy.com/main/code/problem/problemDetail.do?problemLevel=2&contestProbId=AV5PjMgaALgDFAUq&categoryId=AV5PjMgaALgDFAUq&categoryType=CODE&problemTitle=&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=2&pageSize=10&pageIndex=3)
```python
```



## 22) [1928. Base64 Decoder](https://swexpertacademy.com/main/code/problem/problemDetail.do?problemLevel=2&contestProbId=AV5PR4DKAG0DFAUq&categoryId=AV5PR4DKAG0DFAUq&categoryType=CODE&problemTitle=&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=2&pageSize=10&pageIndex=3)
```python
```



## 23) [1288. 새로운 불면증 치료법](https://swexpertacademy.com/main/code/problem/problemDetail.do?problemLevel=2&contestProbId=AV18_yw6I9MCFAZN&categoryId=AV18_yw6I9MCFAZN&categoryType=CODE&problemTitle=&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=2&pageSize=10&pageIndex=3)
```python
```



## 24) [1285. 아름이의 돌 던지기](https://swexpertacademy.com/main/code/problem/problemDetail.do?problemLevel=2&contestProbId=AV18-stqI8oCFAZN&categoryId=AV18-stqI8oCFAZN&categoryType=CODE&problemTitle=&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=2&pageSize=10&pageIndex=3)
```python
```



## 25) [1284. 수도 요금 경쟁](https://swexpertacademy.com/main/code/problem/problemDetail.do?problemLevel=2&contestProbId=AV189xUaI8UCFAZN&categoryId=AV189xUaI8UCFAZN&categoryType=CODE&problemTitle=&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=2&pageSize=10&pageIndex=3)
```python
T = int(input())
for test_case in range(1, T + 1):
    P, Q, R, S, W = map(int, input().split())
    charge_A = P * W
    if W <= R:
        charge_B = Q
    else:
        charge_B = Q + (W - R) * S
    print(f'#{test_case} {min(charge_A, charge_B)}')
```



## 26) [1204. 최빈수 구하기](https://swexpertacademy.com/main/code/problem/problemDetail.do?problemLevel=2&contestProbId=AV13zo1KAAACFAYh&categoryId=AV13zo1KAAACFAYh&categoryType=CODE&problemTitle=&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=2&pageSize=10&pageIndex=3)
```python
# 내 풀이
T = int(input())
for case in range(1, T + 1):
    test_case = int(input())
    scores = list(map(int, input().split()))
    score_count = []
    for i in range(len(scores)):
        score_count.append(scores.count(scores[i]))
    for i in range(len(scores)):
        if score_count[i] == max(score_count):
            print(f'#{test_case} {scores[i]}')
            break
            
# 인터넷의 다른 방법
T = int(input())
for t in range(1,T+1):
    n = input()
    grade_cnt = [0]*101 # 인덱스가 점수. idx=1이 1점을 받은 인원수
    mymax = 0 # 가장 많은 인원 수
    grade = 0 # 그 인원수가 있던 인덱스 번호 => 점수
    arr = list(map(int,input().split())) # 각 값은 100이하, 개수는 1000개
    for i in range(len(arr)):
        grade_cnt[arr[i]] += 1
    for x in range(1,len(grade_cnt)):
        if mymax <= grade_cnt[x]:
            mymax = grade_cnt[x]
            grade = x
 
    print('#{} {}'.format(t, grade))
```