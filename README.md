# lab16.02
Задание 1
from math import sqrt
 
def distance(a, b, c, d):
    return sqrt((a - b) ** 2 + (c - d) ** 2)
 
a = float(input())
b = float(input())
c = float(input())
d = float(input())
print(distance(a, b, c, d))
Задание 2
def min4(a, b, c, d):
    mas = [a,b,c,d]
    mas.sort()
    return mas[0]
 
print(min4(15,4,16,1))
Задание 3
def ipis(a,b):
      if abs(a)<=1 and abs(b)<=1:
            return True
      else:
            return False
 
 def IsPointInSquare(a,b):
      return ipis(a,b)
 Задание 4
 def power(a, n):
    res = 1
    for i in range(abs(n)):
        res *= a
    if n >= 0:
        return res
    else:
        return 1 / res
 
print(power(float(input()), int(input())))
Задание 5
a = int(input())
b = int(input())
 
v = a
g = b
while v != 0 and g != 0:
    if v > g:
        v = v % v
    else:
        g = g % v
 
if a == 0:
    c = v
    print(a // c, b // c)
else:
    c = g
    print(a // c, b // c)
Задание 6
def MinDivisor(n):
    for i in range(2, int(n ** 0.5) + 1):
        if n % i == 0:
            return i
    return n
 
def main():
    n = int(input())
    print(MinDivisor(n))
 
if __name__ == "__main__":
    main()
Задание 7
def Isprime(n):
    i = 2
    j = 0
    while(True):
        if(i*i <= n and j != 1):
            if(n % i == 0):
                j=j+1
            i=i+1
        elif(j==1):
            print('No')
            return False
        else:
            print('Yes')
            return True
Задание 8
def power(a, n):
    if n == 0:
        return 1
    else:
        return a * power(a, n - 1)
 
print(power(float(input()), int(input())))
Задание 9
def C(n, k):
    if k == n or k == 0:
        return 1
    if k != 1:
        return C(n-1, k) + C(n-1, k-1)
    else:
        return n


print(C(int(input()), int(input())))
