<details>
<summary>Editorial</summary>
<br>
It's a very straight forward question. 
We have 2 conditions : 
	<br>
	1. When number is odd , number = number * 3 + 1
	<br>
	2. When number is even , number = number / 2;

Tip :-
-------
<br>
Always check odd : if (n & 1) --> if n is odd this will be even cause LSB (least significant or bit at ones place of odd number is 1 and even is 0) 

</details>

<details>
<summary>Code</summary>
<br>
	
	#include<bits/stdc++.h>
	#define ll long long 
	using namespace std;
 
	int main() {
	
	ios_base::sync_with_stdio(false); 
	cin.tie(NULL);
	
	ll n; cin >> n;
	  cout << n << " ";
	  
	  while (n != 1) {
		if (n&1) {
		    n = n*3 + 1;
		    cout << n << " ";
		} else {
		    n /= 2;
		    cout << n << " ";
		}   
	  } 
	}
</details>
