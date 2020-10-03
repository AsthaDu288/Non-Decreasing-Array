# Non-Decreasing-Array
Given an array nums with n integers, your task is to check if it could become non-decreasing by modifying at most 1 element.
class Solution {
    public boolean checkPossibility(int[] nums) {
        int count =0; //no of modification which is atmost one time
        for(int i=0;i<nums.length-1;i++){
            if(nums[i]>nums[i+1]){
                count++;
                if(count>1){
                    return false;
                }
                if(i>0 && nums[i-1]>nums[i+1]){
                    nums[i+1]=nums[i];
                }
                else{
                    nums[i]=nums[i+1];
                }
            }
        }
                return true;

}
}
