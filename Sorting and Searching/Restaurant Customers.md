<details open>
	<summary>Editorial</summary>
	<ol>
		<li>Make a vector of pair</li>
		<li>Push all the entry times as {entry_time , +1}</li>
		<li>Push all the exit times as {exit_time , -1}</li>
		<li>Sort the array and take sum of the second value of the vector for first <strong>N</strong> values</li>
	</ol>
	<br>
	<h4>Second</h4>

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
	 
		ll n;
		cin >> n;
		vector<pair<ll, ll>> a;
	 
		for (ll i = 0; i < n; i++) {
			ll x , y;
			cin >> x >> y;
			a.push_back({x, 1});
			a.push_back({y, -1});
		}
	 
		sort(a.begin() , a.end());
	 
		ll mx , sum;
		sum = mx = 0;
		for (auto person : a) {
			sum += person.second;
			mx = max(sum , mx);
		}
		if (mx < 0)
			mx = 0;
		cout << mx;
	 
	}

</details>