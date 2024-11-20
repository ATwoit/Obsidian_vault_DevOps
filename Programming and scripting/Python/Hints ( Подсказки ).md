## При математических вычислениях

Когда нужно разделить каждое число по отдельности:
```python
n = int(input()) 
d1 = (n // 10 ** 3) % 10 
d2 = (n // 10 ** 2) % 10 
d3 = (n // 10 ** 1) % 10 
d4 = (n // 10 ** 0) % 10
```

В Python есть встроенная функция `max()`, которая вычисляет максимальное число из переданных ей:
```python
a, b, c, d = int(input()), int(input()), int(input()), int(input()) 
print(max(a, b, c, d))
```

Программа должна вывести минимально возможное количество чеканных монет для оплаты.
```python
n = int(input())
num = 0

# Сначала используем самые большие монеты, чтобы минимизировать их количество
num += n // 25  # Считаем количество монет номиналом 25
n %= 25  # Остаток от деления на 25

num += n // 10  # Считаем количество монет номиналом 10
n %= 10  # Остаток от деления на 10

num += n // 5  # Считаем количество монет номиналом 5
n %= 5  # Остаток от деления на 5

num += n  # Остаток — это количество монет номиналом 1

print(num)
```


Для вычисление факториала без factorial:
```python
n = int(input()) 
res = 1 i = 2 
while i <= n: 
	res *= i     
	i += 1 
print(res)
```

Для преобразование 10-ой системы в двоичною:
```python
n = int(input())
print(format(n, 'b'))
```

Ходы в шахмате:
```python
# Ладья
x1, y1, x2, y2 = int(input()), int(input()), int(input()), int(input())

if x1 == x2 or y1 == y2:
    print("YES")
else:
    print("NO")

# Король
x1, y1, x2, y2 = int(input()), int(input()), int(input()), int(input())
if (-1 <= x2 - x1 <= 1) and (-1 <= y2 - y1 <= 1):
    print('YES')
else:
    print('NO')


# Слон
x1, y1, x2, y2 = int(input()), int(input()), int(input()), int(input())
c1 = x1 - y1
c2 = x2 - y2
c3 = x1 + y1
c4 = x2 + y2

if c1 == c2 or c3 == c4:
    print("YES")
else:
    print("NO")


# Конь
x1, y1, x2, y2 = int(input()), int(input()), int(input()), int(input())

if abs((x1 - x2) * (y1 - y2)) == 2:
    print("YES")
else:
    print("NO")

# Ферзь
x1, y1, x2, y2 = int(input()), int(input()), int(input()), int(input())
c1 = x1 - y1
c2 = x2 - y2
c3 = x1 + y1
c4 = x2 + y2

if c1 == c2 or c3 == c4:
    print("YES")
elif x1 == x2 or y1 == y2:
    print("YES")
else:
    print("NO")

```

Последовательность Фибоначчи:
```python
n = int(input())
f1 = 0
f2 = 1

for i in range(0, n):
    f1, f2 = f2, f1+f2

    print(f1, end=' ')
```

Шифр Цезаря 🌶️
```python
number = int(input())
word = input()

for letter in word:
    letter_code = ord(letter)
    new_letter_code = ord('a') + (letter_code - ord('a') - number) % 26
    print(chr(new_letter_code), end='')

```

