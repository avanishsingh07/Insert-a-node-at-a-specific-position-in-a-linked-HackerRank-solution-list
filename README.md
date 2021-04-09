# Insert-a-node-at-a-specific-position-in-a-linked-HackerRank-solution-list
Insert a node at a specific position in a linked list

static SinglyLinkedListNode insertNodeAtPosition(SinglyLinkedListNode head, int data, int position) {
        SinglyLinkedListNode new_node = new SinglyLinkedListNode(data);
        int count=0;
        if(position == 1){
            new_node.next=head;
            head=new_node;
            return new_node;
        }
        SinglyLinkedListNode previous = head;
        while(count<position-1){
            previous = previous.next;
            count++;
        }
        SinglyLinkedListNode current = previous.next;
        previous.next = new_node;
        new_node.next = current;
        return head;
    }
