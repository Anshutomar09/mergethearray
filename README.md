# mergethearray

class Solution {
public:
    void merge(vector<int>& nums1, int m, vector<int>& nums2, int n) {
        int i=n-1,j=m-1;
        int k=m+n-1;
       while(n>=0 && m>=0){
           if(nums1[i]<nums2[j]){
               nums1[k]=nums1[i];
               i--;
           }
           else{
               nums1[k]=nums2[j];
                j--;     
           }
           k--;
       } 
       while(n>=0){
        nums1[k]=nums1[i];
               i--;
               k--;
       }
       while(m>=0){
           nums1[k]=nums2[i];
                 j--;
                k--;
       }
       
    }
};
