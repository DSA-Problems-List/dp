# 70. Climbing Stairs

## basic solution 

```java
import java.util.Scanner;
public class Climbing_Stairs{
    public static int countStair(int n){
        int ways[] = new int[n+1];
        ways[0]=1;
        
        for(int i = 1 ; i<= n;i++){
            if(i == 1 ){
              ways[i] = ways[i-1]+0;
            }else{
                ways[i]=ways[i-1]+ways[i-2];
            }
        }
        return ways[n];
    }

    public static void main (String[]args){
        Scanner sc = new Scanner(System.in);
        System.out.print("Enter the Stair to go : ");
        int n = sc.nextInt();
        System.out.println(countStair(n));
    }
}
```

## In leetcode :
``` java
public class Solution {
    public int climbStairs(int n) {
      

        int[] ways = new int[n + 1];
        ways[0] = 1;
        

        for (int i = 1; i <= n; i++) {
            if(i==1){
            ways[i]=ways[i-1]+0;
            }else{
            ways[i] = ways[i - 1] + ways[i - 2];
            }
        }

        return ways[n];
    }
}
```