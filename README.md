class Solution
{
    //Function to sort a linked list of 0s, 1s and 2s.
    static Node segregate(Node head)
    {
   ArrayList<Integer> list=new ArrayList<>();

        

        Node curr=head;

        while(curr!=null){

            list.add(curr.data);

            curr=curr.next;

        }

        Collections.sort(list);

        

        Node ans=new Node(list.get(0));

        Node temp=ans;

 

        for(int i=1; i<list.size(); i++){

            temp.next=new Node(list.get(i));

            temp=temp.next;

        } 

        return ans;

    }

}
