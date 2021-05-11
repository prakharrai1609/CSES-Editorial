<details open>
	<summary>Editorial</summary>
	<ul>
		<li>Input 2 arrays , price and budget</li>
		<li>Push the prices in a multiset and sort in decreasing order</li>
		<li>Now find lower bound of every price in the multiset</li>
			<ol>
				<li>If the lower bound of multiset points to end of the set , print -1 and continue</li>
				<li>Otherwise lower bound of multiset will point to the exact price or the price just lower than that (since sorted in decreasing order)</li>
				<li>Then erase the price value</li>
			</ol>
	</ul>
</details>
<br>
<details>
	
	#include<bits/stdc++.h>
	#define ll long long
	#define vcll vector<ll>
	using namespace std;
	 
	void init() {
	#ifndef ONLINE_JUDGE
		freopen("input.txt", "r", stdin);
		freopen("output.txt", "w", stdout);
	#endif
	}
	 
	int main() {
		init();
		ios_base::sync_with_stdio(false); cin.tie(NULL);
	 
		ll n , m;
		cin >> n >> m;
		vcll price(n);
		vcll budget(m);
		multiset<ll , greater<ll>> set;
	 
		for (ll i = 0; i < n; i++) {
			cin >> price[i];
			set.insert(price[i]);
		}
	 
		for (ll i = 0; i < m; i++) {
			cin >> budget[i];
		}
	 
		for (auto x : budget) {
			auto it = set.lower_bound(x);
			if (it == set.end()) {
				cout << -1 << ' ';
				continue;
			}
	 
			cout << *it << ' ';
			set.erase(it);
		}
	 
	}

		
</details>
