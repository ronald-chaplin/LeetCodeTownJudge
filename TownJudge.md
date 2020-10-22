```
class Solution {
    public int findJudge(int N, int[][] trust) {
        
        int[] trustArray = new int[N+1];
        
        for (int[] temp: trust) {
            trustArray[temp[0]]--;
            trustArray[temp[1]]++;
        }
        
        for (int i = 1; i <= N; ++i) {
            if (trustArray[i] == N - 1) 
                return i;
        }
        return -1;
    
                    
        
    }
}
```
