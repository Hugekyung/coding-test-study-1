### ๐ ๋ฌธ์  ์ค๋ช

![img.png](img.png)

### ๐งฐ ๋ณ์ ์ค๋ช

- **N**
  - ํ์ : ์ ์
  - ์ ์ฅ ๋ฐ์ดํฐ : ์๋ ฅ ๋ฐ์ ์ซ์์ ์๋ฅผ ์ ์ฅํฉ๋๋ค.

- **operations**
  - ํ์ : ๋ฆฌ์คํธ
  - ์ ์ฅ ๋ฐ์ดํฐ : ์ฌ์ฉ ๊ฐ๋ฅํ ์ฐ์ฐ์๋ฅผ ๋ชจ์๋์ ๋ฆฌ์คํธ

- **number_input**
  - ํ์ : ๋ฆฌ์คํธ
  - ์ ์ฅ ๋ฐ์ดํฐ : ์๋ ฅ๋ฐ์ ์ซ์๋ฅผ ๋ฆฌ์คํธ๋ก ์ ์ฅ

- **operation_input**
  - ํ์ : ๋ฆฌ์คํธ
  - ์ ์ฅ ๋ฐ์ดํฐ : ์๋ ฅ๋ฐ์ ์ฐ์ฐ์ ๊ฐ์๋ฅผ ๋ฆฌ์คํธ๋ก ์ ์ฅ

- **operation_list**
  - ํ์ : ๋ฆฌ์คํธ
  - ์ ์ฅ ๋ฐ์ดํฐ : ์๋ ฅ๋ฐ์ ์ฐ์ฐ์ ๊ฐ์ ๋งํผ ์ฌ์ฉ๊ฐ๋ฅํ ์ค๋ณต๋์ง ์์ ์กฐํฉ์ ์ ์ฅ

- **result**
  - ํ์ : ์ ์
  - ์ ์ฅ ๋ฐ์ดํฐ : ๊ณ์ฐํ ๊ฐ ์ ์ฅ
  
- **answer**
  - ํ์ : ๋ฆฌ์คํธ
  - ์ ์ฅ ๋ฐ์ดํฐ : ๊ณ์ฐํ ๊ฐ ๋ค์ ์ ์ฅ
### ๐จํ์ด ๊ณผ์ 

```txt
1. ์๋ ฅ๋ฐ์ ๋ณ์๋ค์ ์๋ ฅ ๋ฐ๋๋ค. [ N, number_input, operation_input ]
2. ์ฌ์ฉ ๊ฐ๋ฅํ ์ฐ์ฐ์๋ค์ ์ ์ฅํ๋ค. [ operations ]
3. for๋ฌธ์ ํตํด operation_input ์ ์๋ ฅ๋ ๊ฐ ๋งํผ operations์์ ๊บผ๋ด์ ์ ์ฅํ๋ค.
4. permutations๋ฅผ ํตํด operations์ ์ ์ฅ๋ ๊ฐ ๋ค๋ก ์ฌ์ฉ๊ฐ๋ฅํ ๋ชจ๋  ์กฐํฉ์ ์ ์ฅํ๋ค.
5. ์ด๋ ์ค๋ณต๋ ์กฐํฉ์ด ์์ผ๋ฉด ์๊ฐ์ด ์ด๊ณผ๋๋ฏ๋ก set์ ํตํด ์ค๋ณต์ ์ ๊ฑฐํด์ค๋ค.
6. ์ด์ค for๋ฌธ์ ํตํด ์ฐ์ฐ์๋ฅผ ๋บ ํ ๊ทธ ์ฐ์ฐ์์ ๊ฐ๋ค์ ๊ณ์ฐํ๋ค.
7. answer์ ์ ์ฅ๋ ๊ฐ๋ค์ max์ min์ ํตํด ์ต๋, ์ต์ ๊ฐ์ ์ถ๋ ฅํด์ค๋ค.

```

```python
from itertools import permutations
import sys
N = int(sys.stdin.readline())
operations = ['+', '-', '*', '/']
number_input = list(map(int, sys.stdin.readline().split()))
operations_input = list(map(int, sys.stdin.readline().split()))  # + - * / ์์๋๋ก ์ซ์๋ฅผ ์๋ ฅ

operation_list = []

for i in range(4):
    for j in range(operations_input[i]):
        operation_list.append(operations[i])
print(operation_list)
operation_list = list(set(permutations(operation_list)))
# ๊ฐ๋ฅํ ์กฐํฉ์ ๋ชจ๋ ์ฌ์ฉํ๊ธฐ ์ํด permutations๋ฅผ ์ฌ์ฉํ์ฌ ์กฐํฉ๋ค์ list์ ์ ์ฅ
# ์ด๋ set์ ์ฌ์ฉํ์ง ์๊ณ  ์ค๋ณต๋ ์กฐํฉ๋ค๋ ์ฌ์ฉํ๊ฒ ํ  ์ ์๊ฐ์ด๊ณผ๊ฐ ๋จ๋ฏ๋ก set์ ํตํด ์ค๋ณต์ ์ ๊ฑฐํด์ค๋ค.
answer = []

for i in operation_list:
    result = number_input[0]
    for j in range(N - 1):
        if i[j] == '+':
            result += number_input[j + 1]
        elif i[j] == '-':
            result -= number_input[j + 1]
        elif i[j] == '*':
            result *= number_input[j + 1]
        else:
            if result // number_input[j + 1] < 0:
                result = -(-result // number_input[j + 1])
            else:
                result = result // number_input[j + 1]

    answer.append(result)
print(max(answer))
print(min(answer))

```

์๊ฐ : **608ms**
