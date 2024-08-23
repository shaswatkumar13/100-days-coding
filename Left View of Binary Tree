class Tree
{
    static int h;
    //Function to return list containing elements of left view of binary tree.
    ArrayList<Integer> leftView(Node root)
    {
        h  = 0;
    ArrayList<Integer> list = new ArrayList<>();
    solve(list,root);
    return list;
    }
    public static void solve(ArrayList<Integer> list,Node root){
        if(root == null){
            return;
        }
        if(h>= list.size()){
            list.add(root.data);
        }
        h++;
        solve(list,root.left);
        solve(list,root.right);
        h--;
    }
}
