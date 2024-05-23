# DSA_problems
1480. Running Sum of 1d Array

class Solution {
public:
     vector<int> runningSum(vector<int>& nums) {
        int currentSum=0;
        for(size_t i=0; i<nums.size(); i++){
            currentSum += nums[i];
            nums[i]= currentSum; 
        }
        return nums;
    }
};



1732. Find the Highest Altitude
      
      class Solution {
public:
    int largestAltitude(vector<int>& gain) {
        int max_altitude=0;
        int current_altitude=0;
        for(size_t i=0; i<gain.size(); i++){
            current_altitude += gain[i];
            max_altitude= std::max(max_altitude, current_altitude);
        }
        return max_altitude;
    }
};



2011. Final Value of Variable After Performing Operations

      class Solution {
public:
    int finalValueAfterOperations(vector<string>& operations) {
        int X=0;
        for(int i=0; i<operations.size(); i++){
            if(operations[i]=="X++" || operations[i]=="++X")
            X+=1;
            else 
            X-=1;
        }
        return X;
    }
};

