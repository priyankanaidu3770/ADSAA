import java.util.*;
class MaxHeap
{
    int []arr;
    int heapsize,maxsize;
    MaxHeap(int ms)
    {
        maxsize = ms;
        heapsize = 0;
        arr = new int[maxsize];
    }
    int parent(int i)
    {
        return (i-1)/2;
    }
    int lchild(int i)
    {
        return (2*i+1);
    }
    int rchild(int i)
    {
        return (2*i+2);
    }
    void insertkey(int x)
    {
        if(heapsize==maxsize)
        {
            System.out.println("Exceeding heap size");
            return;
        }
        int i = heapsize;
        arr[i] = x;
        heapsize++;
        while(i!=0 && arr[parent(i)]<arr[i])
        {
            int temp = arr[i];
            arr[i] = arr[parent(i)];
            arr[parent(i)] = temp;
            i = parent(i);
        }
    }
    void removeMax()
    {
        if(heapsize<=0)
            System.out.println("no heap exist");
        else if(heapsize == 1)
            heapsize--;
        else
        {
            arr[0] = arr[heapsize-1];
            heapsize--;
            maxHeapify(0);
        }
    }
    void maxHeapify(int i)
    {
        int l = lchild(i);
        int r = rchild(i);
        int largest = i;
        if(l<heapsize&&arr[l]>arr[largest])
            largest = l;
        if(r<heapsize&&arr[r]>arr[largest])
            largest = r;
        if(largest!=i)
        {
            int temp = arr[largest];
            arr[largest] = arr[i];
            arr[i] = temp;
            maxHeapify(largest);
        }
    }
    int getMax()
    {
        return arr[0];
    }
    int curSize()
    {
        return heapsize;
    }
    public static void main(String args[])
    {
        MaxHeap h = new MaxHeap(15);
        int elements[] = {3,10,12,8,2,14};
        for(int e : elements)
        h.insertkey(e);
        System.out.println("The current size of the heap is "+h.curSize());
        System.out.println("The current maximum element is "+h.getMax());
        h.removeMax();
        System.out.println("The current size of the heap is "+h.curSize());
        h.insertkey(15);
        h.insertkey(5);
        System.out.println("TThe current size of the heap is "+h.curSize());
        System.out.println("The current maximum element is "+h.getMax());
    }
}
