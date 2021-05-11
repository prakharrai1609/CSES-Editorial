<details>
<summary>Editorial</summary>
<br>
As we know , sum of first **N** numbers is <strong>N * (N + 1) / 2</strong> , let's call it sum1 . If we take the sum of the given <strong>N - 1</strong> numbers , let's call it sum2 . <br>
Now , sum1 = sum2 + missing number , so missing numbers -> sum1 - sum 2 .
</details>
<details>
<summary>Code</summary>
	
	#include<bits/stdc++.h>
	#define ll long long 
	using namespace std;
 
	int main() {
	
	ios_base::sync_with_stdio(false); 
	cin.tie(NULL);
	
	    ll n; cin >> n;
	    ll sum = 0;
	    for (ll i = 0; i < n-1; i++) {
	      ll x; cin >> x;
	      sum += x;
	    }
	    ll sum2 = n * (n+1);
	    sum2 /= 2;
	    cout << (sum2 - sum);
	}
</details>
