m = list(map(int, input().split()))
a = m[0]
p = m[1]
arr = []
if a == 1:
    b = list(map(int, input().split()))
    x1 = p / b[1]
    x2 = (p - b[0]*(b[1] - b[2])) / b[2]
    if x1 <= b[0]:
        print(x1.__ceil__())
        exit(0)
    else:
        print(x2.__ceil__())
        exit(0)
if a == 2:
    b = list(map(int, input().split()))
    c = list(map(int, input().split()))
    a1 = b[1]
    a2 = c[1]
    b1 = b[2]
    b2 = c[2]
    z1 = b[0]
    z2 = c[0]
    x1 = p / (a1 + a2)
    x2 = ((p - z1 * (a1 - b1)) / (a2 + b1))
    x3 = ((p - z2 * (a2 - b2)) / (a1 + b2))
    x4 = (p - z1 * (a1 - b1) - z2 * (a2 - b2)) / (b1 + b2)
    if x1 <= z1 and x1 <= z2:
        print(x1.__ceil__())
    elif z1 < x2 <= z1:
        print(x2.__ceil__())
    elif z2 < x3 <= z1:
        print(x3.__ceil__())
    else:
        print(x4.__ceil__())
    exit(0)

flag = True
fs = True
last_z = None
for i in range(a):
    b = list(map(int, input().split()))
    if fs:
        last_z = b[0]
        fs = False
    if last_z != b[0]:
        flag = False
    b.append(b[0] * (b[1] - b[2]))
    arr.append(b)
if flag:
    y = 0
    j = 0
    z = 0
    for elem in arr:
        y += elem[1]
        j += elem[2]
        z = elem[0]
    x1 = p / y
    x2 = (p - z * (y - j)) / j
    if x1 <= z:
        print(x1.__ceil__())
        exit(0)
    else:
        print(x2.__ceil__())
        exit(0)
else:
    for x in range(1, p):
        summa = 0
        for elem in arr:
            if elem[0] < x:
                summa += elem[3] + elem[2] * x
            else:
                summa += elem[1] * x
        if summa >= p:
            print(x)
            break
