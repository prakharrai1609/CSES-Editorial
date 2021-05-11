<details open>
	<summary>Editorial</summary>
	Use 2 pointer method to find 
	<ul>
		<li>Sort the array app (applicant's demand size) and ap (apartment size)</li>
		<li>Make 2 pointers , p1 and p2</li>
		<li>Run p1 on app and p2 on ap</li>
		<ol>
			<li>If size of apartment is valid , increment both p1 and p2</li>
			<li>If apartment is smaller , move p2</li>
			<li>If applicant's need is more , move p1</li>
		</ol>
	</ul>
</details>
<br>
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
			ll n , m , k;
			cin >> n >> m >> k;
			vcll app(n);
			vcll ap(m);
		 
			lol(i, 0, n) {
				cin >> app[i];
			}
		 
			lol(i, 0, m) {
				cin >> ap[i];
			}
		 
			sort(all(app));
			sort(all(ap));
		 
			ll p1 , p2;
			p1 = p2 = 0;
			cnt = 0;
		 
			while (p1 < n and p2 < m) {
				if (abs(app[p1] - ap[p2]) <= k) {
					p1++;
					p2++;
					cnt++;
					continue;
				}
		 
				if (app[p1] - ap[p2] > k) {
					p2++;
				}
		 
				if (ap[p2] - app[p1] > k) {
					p1++;
				}
		 
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