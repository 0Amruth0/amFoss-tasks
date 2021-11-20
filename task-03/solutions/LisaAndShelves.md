x=int(input())
result = []
i = 1
while i*i <= x:
    if x % i == 0:
        result.append(i)
        if x//i != i:
            result.append(x//i)
    i += 1
ans=len(result)
print(ans)

