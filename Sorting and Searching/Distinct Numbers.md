<details open>
	<summary>Editorial</summary>
	<ol>
		<li>Make a variable count = 1</li>
		<li>Compare elements pairwise and increase count when numbers aren't the same</li>
	</ol>
</details>
<br>
<details>
	<summary>Code</summary>

		#include<bits/stdc++.h>
		#define ll long long
		#define ld long double
		#define vcll vector<ll>
		#define pb push_back
		#define lol(i,a,b) for(ll i = a; i < b; i++)
		#define mod 1000000007
		#define mt make_tuple
		#define newl endl
		ll cnt,a,b;
		using namespace std;
		 
		void solve() {
		    ll n; cin >> n;
		    ll a[n];
		    lol(i,0,n) {
		        cin >> a[i];
		    }
		    sort(a,a+n);
		    ll x;
		    x = 1;
		    lol(i,1,n) {
		        if (a[i] != a[i-1]) {
		            x++;
		        }
		    }
		    if (x) cout << x;
		}
		 
		int main() {
		ios_base::sync_with_stdio(false);
		cin.tie(NULL);
		    // int t ; cin >> t;
		    // while(t--)
		    solve();
		}
		
</details>
