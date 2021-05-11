<details>
	<summary>Editorial</summary>
	<br>
	<ol>
		<li>Store 1st character , compare it to all the values .</li>
		<li>If you find a new character , store that and change the count to 1 .</li>
		<li>Find the max count</li>
	</ol>

</details>

<details>
	<summary>Code</summary>

		#include<bits/stdc++.h>
		#define ll long long
		ll cnt,a,b;
		using namespace std;
		 
		void solve() {
		    string s; cin >> s;
		    ll c,ans;
		    ans = 1 , c = 0;
		    char x = 'A';
		    for (char l : s) {
		        if (l == x) {
		            c++;
		        } else {
		            x = l;
		            c = 1;
		        }
		        ans = max(ans , c);
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
