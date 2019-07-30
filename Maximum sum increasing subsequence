#include<stdio.h>

int maxSum(int a[], int n)
{
	int ans = 0;
	int dp[n];
	for(int i = 0; i < n; i++) {
		dp[i] = a[i];
	}
	for(int i = 1; i < n; i++) {
		for(int j  = 0; j < i; j++) {
			if(a[i] > a[j] && dp[i] < dp[j] + a[i]) {
				dp[i] = dp[j] + a[i];
			}
		}
	}
	for(int i = 0; i < n; i++){
		if(ans < dp[i]) {
			ans = dp[i];
		}
	}

	return ans;
}

int main()
{
	int n;
	scanf("%d", &n);
	int a[n];
	for(int i = 0; i < n; i++) {
		scanf("%d", & a[i]);
	}

	printf("Maximum sum = %d\n", maxSum(a, n));

	return 0;
}
