### π λ¬Έμ  μ€λͺ

![img.png](img.png)

### π§° λ³μ μ€λͺ

- **n**
    - νμ : μ μ
    - μ μ₯ λ°μ΄ν° : λ³΄λμ ν¬κΈ°λ₯Ό μλ ₯λ°λλ€.
- candies
    - νμ : λ¦¬μ€νΈ
    - μ μ₯ λ°μ΄ν° : μ¬νμ μμ
- answer
    - νμ : μ μ
    - μ μ₯ λ°μ΄ν° : λ¨Ήμ μ μλ μ¬νμ μ΅λ κ°μ
- count
    - νμ : μ μ
    - μ μ₯ λ°μ΄ν° : μ¬ν κ°μ μΉ΄μ΄νΈ

### π¨νμ΄ κ³Όμ 

```txt
1. λ³΄λ νμ ν¬κΈ° μλ ₯ [ n ]
2. μΊλλ€μ μμ μ μ₯ν  λ¦¬μ€νΈ μ μΈ [ candies ]
3. λ¨Ήμ μ μλ μΊλμ μ΅μ’ κ°μλ₯Ό μ μ₯ν  λ³μ μ μΈ [ answer ]
4. n λ§νΌ λ°λ³΅νλ©° μ¬νλ€μ μμμ μλ ₯λ°λλ€.
5. λ°λ³΅λ¬Έμ ν΅ν΄ λͺκ°μ κ°μ μμ μΊλκ° μ΄μ΄μ§λμ§ νμΈνλ ν¨μ μ μΈ [ search ]
6. nλ§νΌ λ°λ³΅νλ forλ¬Έμ ν΅ν΄ μΊλλ€μ μμΉλ₯Ό λ°κΏκ°λ©° search ν¨μλ₯Ό νΈμΆν΄ μ¬νμ μ΅λ κ°μ μ°ΎκΈ°
7. λͺ¨λ  λ°λ³΅μ΄ μ’λ£λ ν answerμ μ μ₯λ μ΅λ κ°μ μΆλ ₯
```

```python
n = int(input())
candies = []
answer = 1

for i in range(n):
    temp = []
    temp_str = input()
    for j in range(n):
        temp.append(temp_str[j])
    candies.append(temp)


# λͺκ° λ¨Ήμ μ μλμ§ μ°Ύλ ν¨μ
def search():
    global answer
    for i in range(n):
        count = 1
        for j in range(n - 1):
            if candies[i][j] == candies[i][j + 1]:
                count += 1
                answer = max(count, answer)
            else:
                count = 1
    for i in range(n):
        count = 1
        for j in range(n - 1):
            if candies[j][i] == candies[j + 1][i]:
                count += 1
                answer = max(count, answer)
            else:
                count = 1


# [λͺ¨λ  μΈμ ν λ μλ¦¬ λ€μ§μ΄λ³΄κ³  μ°ΎκΈ°]
# κ°λ‘ λ€μ§κΈ°
for i in range(n):
    for j in range(n - 1):
        candies[i][j], candies[i][j + 1] = candies[i][j + 1], candies[i][j]
        search()
        candies[i][j], candies[i][j + 1] = candies[i][j + 1], candies[i][j]

# μΈλ‘ λ€μ§κΈ°
for i in range(n):
    for j in range(n - 1):
        candies[j][i], candies[j + 1][i] = candies[j + 1][i], candies[j][i]
        search()
        candies[j][i], candies[j + 1][i] = candies[j + 1][i], candies[j][i]

print(answer)
```

μκ° : **ms**


