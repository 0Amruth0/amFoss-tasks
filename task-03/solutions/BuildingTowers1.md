n=int(input())
a=list(map(int,input().split()))
c=[]
for i in range(n):
    z=a.count(a[i])
    c.append(z)
total=list(set(a))
print(max(c),len(total))

