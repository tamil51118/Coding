### Leetcode Solution

# findDuplicate
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
## find all Duplicates
'''
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











