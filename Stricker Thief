/*
Problem :
Stickler the thief wants to loot money from a society having n houses in a single line.He is a weird person and follows a 
certain rule when looting the houses. According to the rule, he will never loot two consecutive houses. At the same time, 
he wants to maximize the amount he loots. The thief knows which house has what amount of money but is unable to come up 
with an optimal looting strategy.
*/


#include <iostream>
using namespace std;

// Function defination for finding maximum stolen value by theif.
int maxStolenValue(int arr[], int n)
{
    // If there is only one home then return the value of that house.
    if(n < 2) {
        return arr[0];
    }
    
    // Array to store maximum stolen value till givin house 
    int dp[n];
    
    // Save base conditions for first and second value.
    dp[0] = arr[0];
    dp[1] = max(arr[0], arr[1]);
    
    // Iterate from i = 2 to n.
    for(int i = 2; i < n; i++) {
        
        // maximum value till ith house will be 
        // maximum of (i-1)th house without including current house
        // and inculuding ith house + maxVlue till (i-2)th house.
        dp[i] = max(dp[i-1], dp[i-2] + arr[i]);
    }
    
    // return last value which will be the final Answer
    return dp[n-1];
}

int main() {
    
    // No of house n
    int n;
    cin >> n; 
    
    // Array to store value of all house
    int arr[n];
    
    for(int i = 0; i < n; i++) {
        cin >> arr[i];
    }
    
    // Fuction calling of maxStolenValue() to find maximum stolen value
    cout << maxStolenValue(arr, n) << endl;

	return 0;
}


/*

INPUT:
6
5 5 10 100 10 5

OUTPUT:
110

*/
