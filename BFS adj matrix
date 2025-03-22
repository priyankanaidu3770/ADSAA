import java.util.*;
public class BFSAdjMatrix
{
	private int v;
	private int[][]adj;
	public BFSAdjMatrix(int v)
	{
		this.v=v;
		adj=new int[v][v];
	}
	public void BFS(int start)
	{
		boolean[] visited=new boolean[v];
		Arrays.fill(visited,false);
		Queue<Integer>queue=new LinkedList<>();
		queue.add(start);
		visited[start]=true;
		while(!queue.isEmpty())
		{
			int vis=queue.poll();
			System.out.println(vis+" ");
			for(int i=0;i<v;i++)
				if(adj[vis][i]==1 && !visited[i])
				{
					queue.add(i);
					visited[i]=true;
				}
		}
	}
	public static void main(String[]args)
	{
		Scanner sc=new Scanner(System.in);
		System.out.println("enter number of vertices:");
		int v=sc.nextInt();
		BFSAdjMatrix graph=new BFSAdjMatrix(v);
		System.out.println("enter adjacency matrix:");
		for(int i=0;i<v;i++)
			for(int j=0;j<v;j++)
				graph.adj[i][j]=sc.nextInt();
		System.out.println("enter starting vertex for BFS:");
		int start=sc.nextInt();
		System.out.println("BFS traversal starting from vertex "+start+" : ");
		graph.BFS(start);
		sc.close();
	}
}
