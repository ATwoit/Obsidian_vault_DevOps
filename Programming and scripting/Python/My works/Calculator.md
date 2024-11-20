```python
n1 = int(input())
n2 = int(input())
n = input()

c1 = n1 + n2
c2 = n1 - n2
c3 = n1 * n2

  

if n == "+":
    print(c1)
elif n == "-":
    print(c2)
elif n == "*":
    print(c3)
elif n == "/":
    if n2 != 0:
        print(n1 / n2)
    else:
        print("На ноль делить нельзя!")
else:
    print('Неверная операция')
```
