

class Solution
{
public:
    int pivotIndex(vector<int>& nums)
    {
    int rights=0;
        int lefts=0;
        for(int i=0;i<nums.size();i++)
        {
            rights=rights+nums[i];
        }
        for(int i=0;i<nums.size();i++)
        {
            rights=rights-nums[i];
            if(lefts==rights)
            {
                return i;
        }
        lefts=lefts+nums[i];
        }
        return -1;
    }};
