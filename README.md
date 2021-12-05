k = 0
for i in range(8):
    for j in range(8):
        a = [[0,0,0,0,0,0,0,0],
             [0,1,1,1,1,1,1,0],
             [0,0,0,0,0,0,0,0],
             [0,0,0,0,0,0,0,0],
             [0,0,0,0,0,0,0,0],
             [0,0,0,0,0,0,0,0],
             [0,1,1,1,1,0,0,0],
             [0,0,0,0,0,0,0,0]]
        if a[i][j] == 0:
            f = 1
            i1 = i
            j1 = j
            while f:
                a[i1][j1] = 1
                if i1 < 7 and a[i1+1][j1] == 0:
                    i1 += 1
                elif j1 < 7 and a[i1][j1+1] == 0:
                    j1 += 1
                elif i1 > 0 and a[i1-1][j1] == 0:
                    i1 -= 1
                elif j1 > 0 and a[i1][j1-1] == 0:
                    j1 -= 1
                else:
                    f = 0
        print(a)
        flag = 1
        for t in a:
            if 0 in t:
                flag = 0
                break
        if flag == 1:
            k+=1
            print(k,i,j)
print(k,'otv')

