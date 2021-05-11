<details open>
	<summary>Editorial</summary>
	<br>
	Let's divide the matrix in 2 halves :
	<br>
	<ul>
		<li>First is the upper triangle , which includes the diagonal</li>
		<li>Second is the lower triangle</li>
	</ul> 
	<br>
	If we consider the upper triangle (Above the diagonal , y >= x (x and y are the x and y cordinates)):
	<br>
	<ol>
		<li>All odd y cordinates are squares</li>
		<li>When y is odd , it decreases till the diagonal</li>
			<ul>It decreases by (x - 1) ratio</ul>
		<li>When y is even , it increases till the diagonal</li>
			<ul>It increases as : (y-1) * (y-1) + x --> Basically we are taking the sq. odd y coordinates as reference</ul>
	</ol>
	<br>
	Now in the lower triangle 
	<br>
	<ol>
		<li>All even x coordinates are squares</li>
		<li>When x is even , it decreases as : x * x - (y - 1)</li>
		<li>When x is odd , it increases as : (x - 1) * (x - 1) + y</li>
	</ol>

</details>

<details>
	<summary>Code</summary>

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
			ll x, y;
			cin >> x >> y;
		 
			if (y >= x) {
				if (y & 1) {
					cout << (y * y - (x - 1)) << newl;
				} else {
					cout << ((y - 1) * (y - 1) + x) << newl;
				}
			} else {
				if (x & 1) {
					cout << ((x - 1) * (x - 1) + y) << newl;
				} else {
					cout << (x * x - (y - 1)) << newl;
				}
			}
		 
		}
		 
		// FILE WITH TEST CASE
		 
		void init() {
		#ifndef ONLINE_JUDGGE
			freopen("input.txt", "r", stdin);
			freopen("output.txt", "w", stdout);
		#endif
		}
		 
		int main() {
			// init();
			ios_base::sync_with_stdio(false); cin.tie(0);
			int t; cin >> t;
			while (t--)
				solve();
		}
		/* This is my journey and i shall endure the work to reach the top .*/

</details>
