arr= list(map(int,input().split()))
k=int (input())
sum=0
maxlen=0
left=0
right=0
n=len(arr)
while(right<n):
    sum+=arr[right]
    while(sum>k):
        sum-=arr[left]
        left+=1
    maxlen=max(maxlen,right-left+1)
    right+=1
print(maxlen)

