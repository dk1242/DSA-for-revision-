## Some random tips & tricks:
- For continous subarray of same types, just add the count with each iteration, it will give count of all subarrays possible.
  ```cpp
  for(int i=1;i<n;i++){
      if(s[i]==s[i-1]){
          cnt++;
      }else{
          ans+=((1ll * (cnt)*(cnt+1))/2)%1000000007;
          ans %= (1000000007);
          cnt=1;
      }
  }
  ans+=((1ll*(cnt)*(cnt+1))/2)%1000000007;
  ```
  is same as
  ```cpp
  for(int i=0;i<n;i++){
    if(s[i]==prev){
        cnt++;
    }else{
        cnt=1;
        prev = s[i];
    }
    ans=(ans+cnt)%1000000007;
  }
  ```
- Next
