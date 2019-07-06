/*
Problem: 
Given an array arr of N integers. Find the contiguous sub-array with maximum sum.
*/

#include <iostream>
using namespace std;

int maxSumSubArray(int arr[], int n)
{
    // initialize maxValue as first element.
    int maxValue = arr[0];
    int dp[n];
    
    // Assigning initially value of that position as the sum of single element subarray.
    for(int i = 0; i < n; i++) {
        dp[i] = arr[i];
    }
    
    // Update the  value if we have better subarray.
    for(int i = 1; i < n; i++) {
        if((arr[i] + dp[i-1]) > dp[i]) {
            dp[i] = dp[i-1] + arr[i];
        }
    }
    
    // Finding maximum element in updated dp array.
    for(int i = 0; i < n; i++) {
        if(dp[i] > maxValue) {
            maxValue = dp[i];
        }
    }
    
    // Retrun max value.
    return maxValue;
}

int main() {
    // n = no of element in array.
    int n;
    cin >> n;
    
    //Array to store all emelment of array
    int arr[n];
    for(int i = 0; i < n; i++) {
        cin >> arr[i];
    }
    
    // Function calling.
    cout << maxSumSubArray(arr, n) << endl;

	return 0;
}

/*
INPUT:
4
23 23 -98 5

OUTPUT:
46

*/
