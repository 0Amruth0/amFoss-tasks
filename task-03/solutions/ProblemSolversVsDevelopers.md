n,m=map(int,input().split())
dev=list(map(int,input().split()))
psov=list(map(int,input().split()))
dev=sorted(dev)
psov=sorted(psov)
Y=[]
count=0
for i in dev:
    for j in psov:
        if i<j:
            count+=j
            psov.remove(j)
            Y.append(i)
            break
if len(Y)==len(dev):
    print('YES')
    print(count)
else:
    print('NO')
