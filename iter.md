

1. List's iterator  
```
class ListIterator {
     List<String> myList;
     Int current;


  public ListIterator(List<String> in) {
      this.myList = in;
      this.Current = 0;
  } 
  public boolean hashNext() {
         if(myList == null){
      	  Return false;
         }


         if(current >= myList.size()){
          Return false;
         }else{
          Return true;
        }  
     


}


  public String next() {
          Return myList.get(current ++);
  }
}






//2. LinkedList iterator
//Yu Wang
class ListNode {
  public int value;
  public ListNode next;
}
class LLIterator {
  ListNode cur;
  public LLIterator(ListNode head) {
      this.cur = head;
  }
  public boolean hashNext() {
      if（cur == null){
	return false;
      }
      else{
        return true;
      }
}
  public ListNode next() {
        ListNode pre = cur;
        cur = cur.next;
        return pre;
  }
}






//3. Binary Tree's iterator
//He Zhong
//Level order;
class TreeNode {
  public int value;
  public TreeNode left, right;
}
class TreeIterator {
  private TreeNode root;
  private Queue<TreeNode> q;
  
  public TreeIterator(TreeNode root) {
      this.root = root;
      this.q = new LinkedList<TreeNode>();
      If (root != null) {
          q.add(root);
       }
  }
  public boolean hashNext() {
      return q.isEmpty();
  }
  public TreeNode next() {
       TreeNode temp = q.poll();
       if(temp.left != null) q.add(temp.left);
       if(temp.right != null) q.add(temp.right);
       return temp;
  }
}

//4. Graph Iterator
// Ruoyu Wang
class GraphNode {
	public int value;
	public List<GraphNode> nei;
}
class GraphIterator {


	private List<GraphNode> graph;
	private int counter;


	public GraphIterator(List<GraphNode> graph) {
		this.graph = graph;
		counter = 0;
	}
	public boolean hasNext() {
		if (graph == null || graph.size() == 0 || counter >= graph.size()) {
			return false;
		} else {
			return true;
		}
	}
	public GraphNode next() {
		return graph.get(counter++);
	}
}

//5. List of List Iterator
// Yi Ling
class ListIterator {
	List<List<String>> cur;
	private int listIndex;
	private int elemIndex;
  public ListIterator(List<List<String>> in) {
	this.cur = in;
  }
  public boolean hashNext() {
	return !(listIndex >= cur.size() -1 && elemIndex >= cur.get(cur.size()-1).size());
  }
  public String next() {
	if (listIndex ) {
}
	String temp =  in.get(listIndex).get(elemIndex);
	listIndex++;
	elemIndex++;
	return temp;
}
```

