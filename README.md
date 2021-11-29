# The-one-with-all-candy

#include <bits/stdc++.h>
using namespace std;

#define ll long long
#define ff first
#define ss second
#define pb push_back
#define vi vector<int>
#define ford(i, a, b) for (int i = a; i < b; i++)
int main()
{
    int tc;
    cin >> tc;
    while (tc--)
    {
        int n;
        cin >> n;
        int a[n];
        ford(i, 0, n)
        {
            cin >> a[i];
        }
        sort(a, a + n, greater<int>());
        int j = n - 1;
        while (a[j] == a[n - 1])
            j--;
        ll ans = (ll)n * ((ll)a[n - 1]) + (ll)(j + 1);
        cout << ans << endl;
    }
    return 0;
}
