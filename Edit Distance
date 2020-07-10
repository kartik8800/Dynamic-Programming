/*
    author: kartik8800
*/
 
#include<bits/stdc++.h>
#define ll long long
#define pb push_back
#define fr(a,b) for(int i = a; i < b; i++)
#define rep(i,a,b) for(int i = a; i < b; i++)
#define mod 1000000007
#define inf (1LL<<60)
#define all(x) (x).begin(), (x).end()
#define prDouble(x) cout << fixed << setprecision(10) << x
#define triplet pair<ll,pair<ll,ll>>
#define fast_io ios_base::sync_with_stdio(false);cin.tie(NULL)
using namespace std;
 
int dp[5001][5001];
int solve(int i, int j, string& s1, string& s2)
{
    if(i == s1.length() || j == s2.length())
        return max((int)s2.length() - j, (int)s1.length() - i);
 
    if(dp[i][j] != -1)
        return dp[i][j];
 
    int ans;
    if(s1[i] == s2[j]){
        ans = solve(i+1,j+1,s1,s2);
    }
    else{
        int op1 = 1 + solve(i,j+1,s1,s2);//add
        int op2 = 1 + solve(i+1,j,s1,s2);//remove
        int op3 = 1 + solve(i+1,j+1,s1,s2);//replace
        ans = min(op1,min(op2,op3));
    }
    return dp[i][j] = ans;
}
 
int main() {
   fast_io;
   ll t,n,m,x,i,j,k,q;
   //cin >> t;
   t = 1;
   while(t--)
   {
        memset(dp, -1, sizeof dp);
        string s1,s2;
        cin >> s1 >> s2;
        cout << solve(0,0,s1,s2);
   }
   return 0;
}
