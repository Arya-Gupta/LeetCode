// Time Complexity - Nested loops give us a time complexity of O(N^2).
// Space Complexity - No extra space is used, thus space complexity is O(1).
// Explanation - We loop through the entire array, taking elements one by one as M. Then N = 2 * M. Now we search for N in the entire array except for the index of M.

class Solution {
public:
    bool checkIfExist(vector<int>& arr) {
        int N, M, n = arr.size();
        
        for(int i = 0; i < n; i++){
            M = arr[i];
            N = 2 * M;
            for(int j = 0; j < n; j++)
                if(arr[j] == N && j != i) return true;
        }
        return false;
    }
};

