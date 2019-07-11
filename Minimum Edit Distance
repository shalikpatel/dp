/*

Given two strings str1 and str2 and below operations that can performed on str1. Find minimum number of edits (operations) required to convert ‘str1′ into ‘str2′.

Insert
Remove
Replace
All of the above operations are of cost=1.
Both the strings are of lowercase.

*/

#include <iostream>
using namespace std;

int minimumEdit(string s1, string s2, int n, int m)
{
    int dp[n+1][m+1];
    dp[0][0] = 0;
    for(int i = 1; i <= n; i++) {
        dp[i][0] = i; 
    }
    for(int j = 1; j <=m; j++) {
        dp[0][j] = j;
    }
    
    for(int i = 1; i <= n; i++) {
        for(int j = 1; j <= m; j++) {
            if(s1[i-1] == s2[j-1]) {
                dp[i][j] = dp[i-1][j-1];
            } else {
                dp[i][j] = min(min(dp[i-1][j], dp[i][j-1]), dp[i-1][j-1]) + 1;
            }
        }
    }
    
    return dp[n][m];
}

int main() {
    
    int n, m;
    cin >> n >> m;
    string s1, s2;
    cin >> s1 >> s2;
    
    cout << minimumEdit(s1, s2, n, m) << endl;

	return 0;
}

/*
INPUT:
84 87
lrbbmqbhcdarzowkkyhiddqscdxrjmowfrxsjybldbefsarcbynecdyggxxpklorellnmpapqfwkhopkmcoq 
hnwnkuewhsqmgbbuqcljjivswmdkqtbxixmvtrrbljptnsnfwzqfjmafadrrwsofsbcnuvqhffbsaqxwpqcaceh

OUTPUT:
78

*/
