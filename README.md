#include <iostream>
using namespace std;
int main() {
	ios_base::sync_with_stdio(false);
	cin.tie(NULL);
	int T;
	cin>>T;
	while(T--)
	{
		int N;
		cin>>N;
		int arr[N];
		for(int i=1;i<=N;i++)
		{
			cin>>arr[i];

		}
		long long int prefix[N+1]={0};
		prefix[1]=arr[1];
		for(int i=2;i<=N;i++)
		{
			prefix[i]=prefix[i-1]+arr[i];
		}

		int Q;
		cin>>Q;
		while(Q--){
		long long int L,R;
		cin>>L>>R;
		if(L==1)
		{
			cout<<prefix[R]<<"\n";

		}
		else
		{
			cout<<prefix[R]-prefix[L-1]<<"\n";
		}
		/*int sum=0;
		for(int i=L;i<=R;i++)
		{
			sum=sum+arr[i];
		}

		cout<<sum<<endl;*/

	}
	}
}
				 
#include<bits/stdc++.h>
using namespace std;
int main()
{
    
    int n,k,i,j,c,r;
    cin>>n>>k;
    int a[n],b[k];
    set <int> s;  
    for(i=1;i<=n;i++)
    {
        cin>>a[i];
    }
    for(i=1;i<=k;i++)
    {
        cin>>b[i];
    }
    for(i=1;i<=n;i++)
    {c=0;
        for(j=1;j<=k;j++)
        {
            if(a[i]==b[j])
            {
                c++;
            }
        }if(c==0){
            s.insert(a[i]);
        }
    }
    for(i=1;i<=k;i++)
    {r=0;
        for(j=1;j<=n;j++)
        {
            if(b[i]==a[j])
            {
               r++;
            }
        }if(r==0)
        {
            s.insert(b[i]);
        }
    }
    cout<<s.size();
}				 
				 

	
	#include<bits/stdc++.h>
using namespace std;
int main()
{
    int n,k,i,j,c,r;
    cin>>n>>k;
    int a[n],b[k];
    set <int> s;
    for(i=1;i<=n;i++)
    {
        cin>>a[i];
    }
    for(i=1;i<=k;i++)
    {
        cin>>b[i];
    }
    for(i=1;i<=n;i++)
    {c=0;
        for(j=1;j<=k;j++)
        {
            if(a[i]==b[j])
            {
                c++;
            }
        }if(c==0)
        {
            s.insert(a[i]);
        }
    }
    for(i=1;i<=k;i++)
    {r=0;
        for(j=1;j<=n;j++)
        {
            if(b[i]==a[j])
            {
                r++;
            }
        }if(r==0)
        {
            s.insert(b[i]);
        }
    }
   // cout<<s.size();
    set <int>::iterator it;
    for(it=s.begin();it!=s.end();it++)
    {
        cout<<*it<<" ";
    }
}

	
	#include<bits/stdc++.h>
using namespace std;
int main()
{
    int n,k,i,j,c,r;
    cin>>n>>k;
    int a[n],b[k];
    vector <int> s;
    for(i=1;i<=n;i++)
    {
        cin>>a[i];
    }
    for(i=1;i<=k;i++)
    {
        cin>>b[i];
    }
    for(i=1;i<=n;i++)
    {c=0;
        for(j=1;j<=k;j++)
        {
            if(a[i]==b[j])
            {
                c++;
            }
        }if(c>0)
        {
            s.push_back(a[i]);
        }
    }
    for(i=1;i<=k;i++)
    {r=0;
        for(j=1;j<=n;j++)
        {
            if(b[i]==a[j])
            {
                r++;
            }
        }if(r>0)
        {
            s.push_back(b[i]);
        }
    }
    vector <int>::iterator it;
    for(it=s.begin();it!=s.end();it++)
    {
        cout<<*it<<" ";
    }
}
	
	
	
	
	class Solution {
public:
    int subarraySum(vector<int>& nums, int k) 
    {int c=0;
     int sum;
        for(int i=0;i<nums.size();i++)
        {
            for(int j=i;j<nums.size();j++)
            {
                sum=0;
                for(int l=i;l<=j;l++)
                {
                    sum+=nums[l];
                }
                if(sum==k)
                {
                c++;
                }
            }

        }
        
          return c;
    }
  
};
