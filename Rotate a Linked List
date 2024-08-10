class Solution {
    // Function to rotate a linked list.
    public Node rotate(Node head, int k) {
        for(int i=0;i<k;i++){
            Node p=head;
            head=p.next;
            p.next=null;
            Node t=head;
            while(t.next!=null){
                t=t.next;
            }
            t.next=p;
        }
        return head;
    }
}
