import java.util.*;
public class DFSAdjMatrix
{
	private int v;
	private int[][]adj;
	boolean[] visited;
	public DFSAdjMatrix(int v)
	{
		this.v=v;
		adj=new int[v][v];
		visited=new boolean[v];
		Arrays.fill(visited,false);
	}
	public void DFS(int node)
	{
		visited[node]=true;
		System.out.println(node+" ");
		for(int i=0;i<v;i++)
			if(adj[node][i]==1 && !visited[i])
				DFS(i);
	}
	public static void main(String[]args)
	{
		Scanner sc=new Scanner(System.in);
		System.out.println("enter the number of vertices:");
		int v=sc.nextInt();
		DFSAdjMatrix graph=new DFSAdjMatrix(v);
		System.out.println("enter adjacency matrix:");
		for(int i=0;i<v;i++)
			for(int j=0;j<v;j++)
				graph.adj[i][j]=sc.nextInt();
		System.out.println("DFS traversal starting vertex for DFS:");
		int start=sc.nextInt();
		System.out.println("DFS traversal starting from vertex "+start+" : ");
		graph.DFS(start);
		sc.close();
	}
}
