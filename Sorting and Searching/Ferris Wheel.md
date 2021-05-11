<details open>
	<summary>Editorial</summary>
	<ul>
		<li>Sort the array w (array with weights)</li>
		<li>Make 2 pointers p1 and p2</li>
		<li>p1 = 0 , p2 = n - 1</li>
		<ol>	
			<li>If sum w[p1] + w[p2] <= x , increment p1 and decrement p2</li>
			<li>Otherwise decrement p2 only</li>
			<li><strong>If p1 == p2 , compare w[p1] <= x</strong></li>
		</ol>
	</ul>
</details>
<br>
<details>
	
		/*    Author : Prakhar Rai    */
		#include<bits/stdc++.h>
		#define ll long long
		#define ld long double
		#define LB(x,num) lower_bound(x.begin(),x.end(),num) - x.begin()
		#define UB(x,num) upper_bound(x.begin(),x.end(),num) - x.begin()
		#define BS(x,num) binary_search(x.begin(),x.end(),num)
		#define pb push_back
		#define mp make_pair
		#define fs first
		#define sc second
		#define vci vector<int>
		#define vcll vector<ll>
		#define vcd vector<long double>
		#define line(x) sort(x.begin(),x.end())
		#define all(x) x.begin(),x.end()
		#define newl "\n"
		#define vc vector
		#define loop(i,a,b) for(int i = a; i < b; i++)
		#define lol(i,a,b) for(ll i = a; i < b; i++)
		#define lod(i,a,b) for(ld i = 0; i < b; i++)
		#define mod 1000000007
		#define read(v,n) lol(i,0,n) {ll x; cin >> x; v.pb(x);}
		#define run(a,x) for(auto x : a)
		#define yes "YES"
		#define no "NO"
		ll cnt;
		using namespace std;
		// ll dp[10000000];
		// memset(dp, -1, sizeof(dp));
		 
		void solve() {
			ll n , x;
			cin >> n >> x;
			vcll w(n);
		 
			lol(i, 0, n) {
				cin >> w[i];
			}
		 
			sort(all(w));
		 
			ll p1 , p2;
			p1 = 0 , p2 = n - 1;
			cnt = 0;
		 
			while (p1 <= p2) {
				if (w[p1] + w[p2] <= x) {
					p1++;
					p2--;
					cnt++;
					continue;
				}
		 
				if (p1 == p2) {
					if (w[p1] <= x) {
						cnt++;
						break;
					}
				}
		 
				p2--;
				cnt++;
			}
		 
			cout << cnt;
		 
		 
		}
		 
		// FILE WITH TEST CASE
		 
		void init() {
		#ifndef ONLINE_JUDGE
			freopen("input.txt", "r", stdin);
			freopen("output.txt", "w", stdout);
		#endif
		}
		 
		int main() {
			init();
			ios_base::sync_with_stdio(false); cin.tie(0);
			solve();
		}
		/* This is my journey and i shall endure the work to reach the top .*/

</details>