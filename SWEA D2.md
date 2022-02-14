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



## 10) [1979. 어디에 단어가 들어갈 수 있을까](https://swexpertacademy.com/main/code/problem/problemDetail.do?problemLevel=2&contestProbId=AV5PuPq6AaQDFAUq&categoryId=AV5PuPq6AaQDFAUq&categoryType=CODE&problemTitle=&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=2&pageSize=10&pageIndex=1)

```python
T = int(input())
for tc in range(1, T+1):
    N, K = map(int, input().split())
    arr = [[0]*(N+2)] + [[0]+list(map(int, input().split()))+[0] for _ in range(N)] + [[0]*(N+2)]
    cnt = 0
    for i in range(N+2):
        for j in range(N-K+3):
            check = 0
            for k in range(K):
                check += arr[i][j+k]
            if check == K:
                if arr[i][j+K] == 0 and arr[i][j-1] == 0:
                    cnt += 1

    for i in range(N+2):
        for j in range(N-K+3):
            check = 0
            for k in range(K):
                check += arr[j+k][i]
            if check == K:
                if arr[j+K][i] == 0 and arr[j-1][i] == 0:
                    cnt += 1
    print(f'#{tc} {cnt}')
```



## 11) [1976. 시각 덧셈](https://swexpertacademy.com/main/code/problem/problemDetail.do?problemLevel=2&contestProbId=AV5PttaaAZIDFAUq&categoryId=AV5PttaaAZIDFAUq&categoryType=CODE&problemTitle=&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=2&pageSize=10&pageIndex=2)
```python
T = int(input())
for tc in range(1, T+1):
    t1, m1, t2, m2 = map(int, input().split())
    time = t1 + t2

    minute = m1 + m2
    if minute > 60:
        time += 1
        minute -= 60

    if time > 12:
        time -= 12

    print(f'#{tc} {time} {minute}')
```



## 12) [1974. 스도쿠 검증](https://swexpertacademy.com/main/code/problem/problemDetail.do?problemLevel=2&contestProbId=AV5Psz16AYEDFAUq&categoryId=AV5Psz16AYEDFAUq&categoryType=CODE&problemTitle=&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=2&pageSize=10&pageIndex=2)
```python
T = int(input())
for tc in range(1, T+1):
    arr = [list(map(int, input().split())) for _ in range(9)]
    result = 1
    for i in range(9):
        for j in range(8):
            for k in range(j+1, 9):
                if arr[i][j] == arr[i][k]:
                    result = 0
                    break

    for i in range(9):
        for j in range(8):
            for k in range(j + 1, 9):
                if arr[j][i] == arr[k][i]:
                    result = 0
                    break

    for i in range(0, 9, 3):
        for j in range(0, 9, 3):
            numbers = []
            for k in range(3):
                for l in range(3):
                    numbers.append(arr[i+k][j+l])
            if len(set(numbers)) != 9:
                result = 0
                break

    print(f'#{tc} {result}')
```



## 13) [1970. 쉬운 거스름돈](https://swexpertacademy.com/main/code/problem/problemDetail.do?problemLevel=2&contestProbId=AV5PsIl6AXIDFAUq&categoryId=AV5PsIl6AXIDFAUq&categoryType=CODE&problemTitle=&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=2&pageSize=10&pageIndex=2)
```python
T = int(input())
money = [50000, 10000, 5000, 1000, 500, 100, 50, 10]
for tc in range(1, T+1):
    N = int(input())
    cnt = []
    for i in range(8):
        cnt.append(N//money[i])
        N %= money[i]
    print(f'#{tc}')
    print(*cnt)
```



## 14) [1966. 숫자를 정렬하자](https://swexpertacademy.com/main/code/problem/problemDetail.do?problemLevel=2&contestProbId=AV5PrmyKAWEDFAUq&categoryId=AV5PrmyKAWEDFAUq&categoryType=CODE&problemTitle=&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=2&pageSize=10&pageIndex=2)
```python
T = int(input())
for tc in range(1,T+1):
    N = int(input())
    nums = list(map(int,input().split()))
    nums.sort()
    ans =  ' '.join(map(str, nums))
    print(f'#{tc} {ans}')
```



## 15) [1961. 숫자 배열 회전](https://swexpertacademy.com/main/code/problem/problemDetail.do?problemLevel=2&contestProbId=AV5Pq-OKAVYDFAUq&categoryId=AV5Pq-OKAVYDFAUq&categoryType=CODE&problemTitle=&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=2&pageSize=10&pageIndex=2)
```python
T = int(input())
for tc in range(1,T+1):
    N = int(input())
    matrix = []
    for i in range(N):
        row = list(map(str, input().split()))
        matrix.append(row)
    print(f'#{tc}')
    result = [(['']*3) for _ in range(N)]

    for i in range(N):
        for j in range(N):
            result[i][0] += matrix[N-j-1][i]

    for i in range(N):
        for j in range(N):
            result[i][1] += matrix[N-i-1][N-j-1]

    for i in range(N):
        for j in range(N):
            result[i][2] += matrix[j][N-i-1]

    for i in range(N):
        print(*result[i])
```



## 16) [1959. 두 개의 숫자열](https://swexpertacademy.com/main/code/problem/problemDetail.do?problemLevel=2&contestProbId=AV5PpoFaAS4DFAUq&categoryId=AV5PpoFaAS4DFAUq&categoryType=CODE&problemTitle=&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=2&pageSize=10&pageIndex=2)
```python
T = int(input())
for tc in range(1, T+1):
    N, M = map(int, input().split())
    A = list(map(int, input().split()))
    B = list(map(int, input().split()))

    if N >= M:
        result_box = []
        for i in range(N-M+1):
            result = 0
            for j in range(M):
                result += (B[j] * A[j+i])
            result_box.append(result)
        max_result = max(result_box)

    else:
        result_box = []
        for i in range(M-N+1):
            result = 0
            for j in range(N):
                result += (A[j] * B[j+i])
            result_box.append(result)
        max_result = max(result_box)

    print(f'#{tc} {max_result}')
```



## 17) [1954. 달팽이 숫자](https://swexpertacademy.com/main/code/problem/problemDetail.do?problemLevel=2&contestProbId=AV5PobmqAPoDFAUq&categoryId=AV5PobmqAPoDFAUq&categoryType=CODE&problemTitle=&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=2&pageSize=10&pageIndex=2)
```python
# 처음 했던 짓
T = int(input())
import copy
for tc in range(1, T+1):
    N = int(input())
    snail_line = [0]*N
    snail = []
    for i in range(N):
        snail.append(copy.deepcopy(snail_line))

    for i in range(N):
        snail[0][i] += i+1
    for i in range(N-1):
        snail[i+1][N-1] += N+i+1
    for i in range(N-1):
        snail[N-1][N-i-2] += 2*N+i
    for i in range(N-2):
        snail[N-i-2][0] += 3*N+i-1
    
    ...
    
## while 돌려도 안으로 들어가는 게 좀 무리 같아서 마지막 숫자부터 집어넣어봄
import copy
T = int(input())
for tc in range(1, T+1):
    N = int(input())
    print(f'#{tc}')
    snail_line = [0]*N
    snail = []
    for i in range(N):
        snail.append(copy.deepcopy(snail_line)) # 이중 리스트를 만들고 싶어서 딥카피를 했는데 알고보니 다른 잡기술이 있었다
    last = N ** 2

    if N % 2:
        a = N//2
        b = N//2
        snail[a][b] = last
        num = 1
        cnt = 0
        while 1: # break 나올때까지 돌린다는 마인드
            cnt += 1
            for i in range(cnt-1): # 왼쪽. 왼쪽으로 갈때는 항상 마지막 줄(시작점이 있는 줄)일수도 있으니
                b -= 1
                last -= 1
                snail[a][b] = last
            if last == 1:
                break
            else:
                b -= 1
                last -= 1
                snail[a][b] = last
            for i in range(cnt): # 아래쪽
                a += 1
                last -= 1
                snail[a][b] = last
            cnt += 1
            for i in range(cnt): # 오른쪽
                b += 1
                last -= 1
                snail[a][b] = last
            for i in range(cnt): # 위쪽
                a -= 1
                last -= 1
                snail[a][b] = last
        for i in range(N):
            print(*snail[i])

    else:
        a = N//2
        b = N//2 - 1
        snail[a][b] = last
        num = 1
        cnt = 0
        while 1:
            cnt += 1
            for i in range(cnt): # 오른쪽
                b += 1
                last -= 1
                snail[a][b] = last
            for i in range(cnt): # 위쪽
                a -= 1
                last -= 1
                snail[a][b] = last
            cnt += 1
            for i in range(cnt-1): # 왼쪽. 마찬가지로 마지막일 수도 있으니
                b -= 1
                last -= 1
                snail[a][b] = last
            if last == 1:
                break
            else:
                b -= 1
                last -= 1
                snail[a][b] = last
            for i in range(cnt): # 아래쪽
                a += 1
                last -= 1
                snail[a][b] = last
        for i in range(N):
            print(*snail[i])

# 이렇게 하는거 맞냐..? 알고리즘 배워서 다시 해봐야 할듯
```

```python
# 알고리즘 배운 후
T = int(input())
for tc in range(1,T+1):
    N = int(input())

    arr = [[0]*N for _ in range(N)] # 2차원 배열 만들기
    di = [0, 1, 0, -1] # 우 하 좌 상(달팽이의 움직이는 순서)
    dj = [1, 0, -1, 0]
    cnt = 1
    i = j = 0
    arr[i][j] = 1

    while 1:
        for k in range(4):
            while 1:
                cnt += 1
                i += di[k]
                j += dj[k]
                if 0<=i<N and 0<=j<N and arr[i][j] == 0: # i와 j가 가능한 수이고 arr[i][j]가 비어있다면
                    arr[i][j] = cnt
                else: # 아니라면 더해준 것들을 모두 원상태로
                    cnt -= 1
                    i -= di[k]
                    j -= dj[k]
                    break
        if cnt == N**2: # N의 제곱수까지 다 넣었으면 break
            break

    print(f'#{tc}')
    for i in range(N):
        print(*arr[i])
```



## 18) [1948. 날짜 계산기](https://swexpertacademy.com/main/code/problem/problemDetail.do?problemLevel=2&contestProbId=AV5PnnU6AOsDFAUq&categoryId=AV5PnnU6AOsDFAUq&categoryType=CODE&problemTitle=&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=2&pageSize=10&pageIndex=2)
```python
mth = [31, 28, 31, 30, 31, 30, 31, 31, 30, 31, 30, 31]
T = int(input())
for tc in range(1, T+1):
    m1, d1, m2, d2 = map(int, input().split())
    result = 1
    if m2 - m1 >= 2:
        for i in range(m1+1, m2):
            result += mth[i-1]
        result += (mth[m1-1] - d1 + d2)
    if m2 - m1 == 1:
        result += (mth[m1-1] - d1 + d2)
    if m1 == m2:
        result += (d2 - d1)
    print(f'#{tc} {result}')
```



## 19) [1946. 간단한 압축 풀기](https://swexpertacademy.com/main/code/problem/problemDetail.do?problemLevel=2&contestProbId=AV5PmkDKAOMDFAUq&categoryId=AV5PmkDKAOMDFAUq&categoryType=CODE&problemTitle=&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=2&pageSize=10&pageIndex=2)
```python
T = int(input())
for tc in range(1, T+1):
    N = int(input())
    alphas = []
    for i in range(N):
        alp, x = map(str, input().split())
        num = int(x)
        alphas.extend([alp]*num)
    print(f'#{tc}')
    while alphas:
        new_alphas = []
        for i in range(10):
            if alphas:
                new_alphas.append(alphas.pop(0))
        print(''.join(new_alphas))
```



## 20) [1945. 간단한 소인수분해](https://swexpertacademy.com/main/code/problem/problemDetail.do?problemLevel=2&contestProbId=AV5Pl0Q6ANQDFAUq&categoryId=AV5Pl0Q6ANQDFAUq&categoryType=CODE&problemTitle=&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=2&pageSize=10&pageIndex=2)
```python
T = int(input())
for tc in range(1, T+1):
    N = int(input())
    a = b = c = d = e = 0

    while not N % 2:
        N /= 2
        a += 1

    while not N % 3:
        N /= 3
        b += 1

    while not N % 5:
        N /= 5
        c += 1

    while not N % 7:
        N /= 7
        d += 1

    while not N % 11:
        N /= 11
        e += 1

    print(f'#{tc} {a} {b} {c} {d} {e}')
```



## 21) [1940. 가랏! RC카!](https://swexpertacademy.com/main/code/problem/problemDetail.do?problemLevel=2&contestProbId=AV5PjMgaALgDFAUq&categoryId=AV5PjMgaALgDFAUq&categoryType=CODE&problemTitle=&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=2&pageSize=10&pageIndex=3)
```python
T = int(input())
for tc in range(1, T+1):
    N = int(input())

    v = 0
    d = 0
    for command in range(N):
        com = list(map(int, input().split()))

        if not com[0]:
            d += v

        if com[0] == 1:
            v += com[1]
            d += v

        if com[0] == 2:
            if v - com[1] > 0:
                v -= com[1]
            else:
                v = 0
            d += v

    print(f'#{tc} {d}')
```



## 22) [1928. Base64 Decoder](https://swexpertacademy.com/main/code/problem/problemDetail.do?problemLevel=2&contestProbId=AV5PR4DKAG0DFAUq&categoryId=AV5PR4DKAG0DFAUq&categoryType=CODE&problemTitle=&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=2&pageSize=10&pageIndex=3)
```python
decoder = ['A', 'B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J', 'K', 'L', 'M', 'N', 'O', 'P', 'Q', 'R', 'S', 'T', 
'U', 'V', 'W', 'X', 'Y', 'Z', 'a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 
'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z', '0', '1', '2', '3', '4', '5', '6', 
'7', '8', '9', '+', '/']

T = int(input())
for test_case in range(1, T + 1):
    encoded_str = input()
    new_str = ''

    bin_str = ''
    for char in encoded_str:
        bin_char = bin(decoder.index(char))[2::]
        while len(bin_char) < 6:
            bin_char = '0' + bin_char
        bin_str += bin_char

    decoded_bin_char = ''
    for i in range(0, len(bin_str), 8):
        decoded_bin_char = ''
        for j in range(i, i+8):
            decoded_bin_char += bin_str[j]
        new_str += chr(int(decoded_bin_char, 2))
    
    print(f'#{test_case} {new_str}')
```



## 23) [1288. 새로운 불면증 치료법](https://swexpertacademy.com/main/code/problem/problemDetail.do?problemLevel=2&contestProbId=AV18_yw6I9MCFAZN&categoryId=AV18_yw6I9MCFAZN&categoryType=CODE&problemTitle=&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=2&pageSize=10&pageIndex=3)
```python
T = int(input())
for test_case in range(1, T + 1):
    N = int(input())
    want_list = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
    x = 1
    sheep_list = []
    while sheep_list != want_list:
        for char in str(x * N):
            if int(char) not in sheep_list:
                sheep_list.append(int(char))
        sheep_list.sort()
        x += 1
    print(f'#{test_case} {(x-1) * N}')
```



## 24) [1285. 아름이의 돌 던지기](https://swexpertacademy.com/main/code/problem/problemDetail.do?problemLevel=2&contestProbId=AV18-stqI8oCFAZN&categoryId=AV18-stqI8oCFAZN&categoryType=CODE&problemTitle=&orderBy=FIRST_REG_DATETIME&selectCodeLang=ALL&select-1=2&pageSize=10&pageIndex=3)
```python
T = int(input())
for test_case in range(1, T + 1):
    N = int(input())
    rocks = list(map(int, input().split()))
    dis_rocks = []
    for i in range(N):
        dis_rocks.append(abs(rocks[i]))
    shortest = min(dis_rocks)
    cnt = dis_rocks.count(shortest)
    print(f'#{test_case} {shortest} {cnt}')
    
# 파이썬으로 풀게 만든 문제가 아닌듯?
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