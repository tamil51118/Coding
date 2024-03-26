###Leetcode Solution

#findDuplicate
*Easy
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
