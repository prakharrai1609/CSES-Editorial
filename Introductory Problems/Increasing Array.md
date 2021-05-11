<details open>
	<summary><strong>Editorial</strong></summary>
	<ol>
		<li>Maintain a variable sum (sum = 0 initially)</li>
		<li>While traversing the array , compare if the current number is greater than previous .</li>
		<li>If the number is greater than the current number , add the difference to sum (sum += (current number - previous number)</li>
	</ol>
	
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
		    ll a[n];
		    lol(i,0,n) {
		        cin >> a[i];
		    }
		    ll c=0;
		    ll ans = 0;
		    lol(i,1,n) {
		        if (a[i]<a[i-1]) {
		            c = (a[i-1]-a[i]);
		            a[i] += c;
		            ans += c;
		        }
		    }
		    cout << ans;
		}
		 
		int main() {
		ios_base::sync_with_stdio(false);
		cin.tie(NULL);
		    // int t ; cin >> t;
		    // while(t--)
		    solve();
		}

</details>
