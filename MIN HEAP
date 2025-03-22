import java.util.Arrays;
class MinHeap
{
	int[] arr;
	int heapsize,maxsize;
	MinHeap(int ms)
	{
		maxsize=ms;
		heapsize=0;
		arr=new int[maxsize];
	}
	int parent(int i)
	{
		return(i-1)/2;
	}
	int lchild(int i)
	{
		return(2*i+1);
	}
	int rchild(int i)
	{
		return(2*i+2);
	}
	void insertkey(int x)
	{
		if(heapsize==maxsize)
		{
			System.out.println("Exceeding heap size");
			return;
		}
		int i=heapsize;
		arr[i]=x;
		heapsize++;
		while(i!=0 && arr[parent(i)]>arr[i])
		{
			int temp = arr[i];
			arr[i]=arr[parent(i)];
			arr[parent(i)]=temp;
			i=parent(i);
		}
	}
	void removeMin()
	{
		if(heapsize<=0) 
			System.out.println("no heap exist");
		else if(heapsize==1)
			heapsize--;
		else
		{
			arr[0]=arr[heapsize-1];
			heapsize--;
			minHeapify(0);
		}
	}
	void minHeapify(int i)
	{
		int l=lchild(i);
		int r=rchild(i);
		int smallest=i;
		if(l<heapsize && arr[l]<arr[i])
			smallest=l;
		if(r<heapsize && arr[r]<arr[smallest])
			smallest=r;
		if(smallest!=i)
		{
			int temp=arr[smallest];
			arr[smallest]=arr[i];
			arr[i]=temp;
			minHeapify(smallest);
		}
	}
	int getMin()
	{
		return arr[0];
	}
	int curSize()
	{
		return heapsize;
	}
	public static void main(String args[])
	{
		MinHeap h = new MinHeap(15);
		int elements[] = {3,10,12,8,2,14};
		for(int e : elements)
			h.insertkey(e);
		System.out.println("The current size of the heap is "+h.curSize());
		System.out.println("The current maximum element is "+h.getMin());
		h.removeMin();
		System.out.println("The current size of the heap is "+h.curSize());
		h.insertkey(15);
		h.insertkey(5);
		System.out.println("THe current size of the heap is "+h.curSize());
		System.out.println("The current maximum element is "+h.getMin());
	}
}
