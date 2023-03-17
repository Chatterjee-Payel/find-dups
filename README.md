# find-dups
  public:
    vector<int> duplicates(int arr[], int n) {
        // code here
       unordered_map<int,int>mp;
       vector<int>ans;
       for(int i=0;i<n;i++){
           mp[arr[i]]++;
       }
       for(auto i:mp)
       {
           if(i.second>1)
           {
              ans.push_back(i.first);
           }
       }
      sort(ans.begin(),ans.end());
      if(ans.empty())
      {
          return {-1};
      }
    return ans;
    }    
};
