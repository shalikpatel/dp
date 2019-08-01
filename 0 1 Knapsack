/*
You are given weights and values of N items, put these items in a knapsack of 
capacity W to get the maximum total value in the knapsack. 
Note that we have only one quantity of each item.
*/

#include<iostream>
using namespace std;

int knapsack(int value[], int weight[], int n, int w)
{
    int dp[n+1][w+1];
    for(int i = 0; i <= n; i++) {
        dp[i][0] = 0;
    }
    for(int j = 0; j <= w; j++) {
        dp[0][j] = 0;
    }
    
    
    for(int i = 1; i <= n; i++) {
        for(int j = 1; j <= w; j++) {
            if(j < weight[i-1]) {
                dp[i][j] = dp[i-1][j];
            } else {
                dp[i][j] = max(dp[i-1][j], dp[i-1][j-weight[i-1]] + value[i-1]);
            }
        }
    }
    
    return dp[n][w];
}

int main()
 {
     int n, w;
     cin >> n >> w;
     int value[n], weight[n];
     
     for(int i = 0; i < n; i++) {
         cin >> value[i];
     }
     for(int i = 0; i < n; i++) {
         cin >> weight[i];
     }
     
     cout << knapsack(value, weight, n, w) << endl;
 
	return 0;
}
