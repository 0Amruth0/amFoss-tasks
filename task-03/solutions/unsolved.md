#Ram and Gifts

t=int(input())
for i in range(t):
    a,b,c,d,N=map(int,input().split())
    if N>=3:
        print(a*c+b*d)
