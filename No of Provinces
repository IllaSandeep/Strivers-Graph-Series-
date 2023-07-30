class Solution {
  public:
    void dfs(int node,vector<int>adj[],int vis[])
    {
        vis[node]=1;
        for(auto it: adj[node])
        {
            if(!vis[it])
            {
                dfs(it,adj,vis);
            }
        }
    }
    int numProvinces(vector<vector<int>> mat, int V) {
        // code here
        vector<int>adj[V];
        for(int i=0;i<V;i++)
        {
            for(int j=0;j<V;j++)
            {
                if(mat[i][j]==1 and i!=j)
                {
                    adj[i].push_back(j);
                }
            }
        }
        int vis[V]={0};
        int c=0;
        for(int i=0;i<V;i++)
        {
            if(!vis[i])
            {
                c++;
                dfs(i,adj,vis);
            }
        }
        return c;
        
    }
};
