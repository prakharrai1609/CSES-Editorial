<details open>
	<summary>Editorial</summary>
	<ol>
		<li>If n == 1 , then straight away output 1</li>
		<li>If n < 4 and n > 1 , then output <strong>NO SOLUTION</strong></li>
		<li>Otherwise , print all evens first and then odd , this will make sure that difference is > 1</li>
	</ol>	
	<br>
	<h3>For ex. </h3>
	<br>
	<p>If n = 6 --> 2 4 6 1 3 5<br>If n = 7 , --> 2 4 6 1 3 5 7</p>

</details>

<details>
	<summary>Code</summary>

	#include<bits/stdc++.h>
	#define ll long long
	#define ld long double
	#define vcll vector<ll>
	#define pb push_back
	#define lol(i,a,b) for(ll i = a; i < b; i++)
	#define mod (1e7+7)
	#define mt make_tuple
	#define newl endl
	ll cnt,a,b;
	using namespace std;
	 
	void solve() {
	    ll n; cin >> n;
	    if (n == 1) cout << 1;
	    else if (n < 4) cout << "NO SOLUTION";
	    else {
	        if (n&1) {
	            ll x = n-1;
	            cout << x << " ";
	            for (ll i = 2; i < x; i+=2) {
	                cout << i << " ";
	            }
	            cout << n << " ";
	            for (ll i = 1; i < x; i += 2) {
	                cout << i << " ";
	            }
	        } else {
	            for (ll i = n-1; i > 0; i-=2) {
	                cout << i << " ";
	            }
	            for (ll i = n; i > 1; i-=2) {
	                cout << i << " ";
	            }
	        }
	    }
	}
	 
	int main() {
	ios_base::sync_with_stdio(false);
	cin.tie(NULL);
	    // int t ; cin >> t;
	    // while(t--)
	    solve();
	}
	
</details>
