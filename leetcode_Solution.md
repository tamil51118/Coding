### Leetcode Solution

# FindDuplicate in an Array
Easy
```
class Solution {
    public int findDuplicate(int[] nums) {
      boolean [] num=new boolean[nums.length+1];
        for(int i:nums){
            if(num[i]==false){
                num[i]=true;

            }
            else{
                return i;
            }
        }
return -1;
    }
}
```
-----------------------------------------------------------------------------------------------------
## Find All Duplicates in an Array
```
class Solution {
    public List<Integer> findDuplicates(int[] nums) {
      boolean [] num=new boolean[nums.length+1];
      List<Integer> arr=new ArrayList<>();
            for(int i:nums){
        if(num[i]==false){
            num[i]=true;
        }
        else{
          arr.add(i);
        }
      }
      return arr;
    }
}
```
--------------------------------------------------------------------------------------------------
# MaximumOddBinaryNumber

```


 public String maximumOddBinaryNumber(String s) {
        StringBuilder sb=new StringBuilder();
        int count=0;
        for(int i=0;i<s.length();i++){
            if(s.charAt(i)=='1'){
                count +=1;
                }

        }
        if(count==0) return "";

        for(int i=1;i<count;i++){
            sb.append(1);
        }
        for(int i=count;i<s.length();i++){
            sb.append(0);
        }
        sb.append(1);
         return sb.toString();  
    }
```
# Square of a Sort Array
```

class Solution {
    public int[] sortedSquares(int[] nums) {
        if(nums == null || nums.length == 0) return nums;
        
        int[] results = new int[nums.length];
        
        int left = 0;
        int right = nums.length-1;
        int i = nums.length-1;
        
        while(left <= right) {
            int leftSquare = nums[left]*nums[left];
            int rigthSquare = nums[right]*nums[right];
            
            if (leftSquare > rigthSquare) {
                results[i--] = leftSquare;
                left++;
            } else {
                results[i--] = rigthSquare;
                right--;
            }
        }
        
        return results;
    }

```












