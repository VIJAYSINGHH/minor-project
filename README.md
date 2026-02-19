#include<iostream>
using namespace std;

struct Node {
  int data;
  Node* next;
};

void printList(Node* head) {
  Node* temp = head;
  while (temp != NULL) {
    cout << temp->data << " ";
    temp = temp->next;
  }
  cout << endl;
}

int main()
{
  // List 1: 9
  Node* head1 = new Node();
  head1->data = 9;
  head1->next = NULL;
  printList(head1);

  // List 2: 5 -> 9
  Node* head2 = new Node();
  head2->data = 5;
  head2->next = new Node();
  head2->next->data = 9;
  head2->next->next = NULL;
  printList(head2);

  // List 3: 8 -> 5 -> 9
  Node* head3 = new Node();
  head3->data = 8;
  head3->next = new Node();
  head3->next->data = 5;
  head3->next->next = new Node();
  head3->next->next->data = 9;
  head3->next->next->next = NULL;
  printList(head3);

  // List 4: 8 -> 5 -> 9 -> 1
  Node* head4 = new Node();
  head4->data = 8;
  head4->next = new Node();
  head4->next->data = 5;
  head4->next->next = new Node();
  head4->next->next->data = 9;
  head4->next->next->next = new Node();
  head4->next->next->next->data = 1;
  head4->next->next->next->next = NULL;
  printList(head4);

  // List 5: 8 -> 5 -> 9 -> 1 -> 12
  Node* head5 = new Node();
  head5->data = 8;
  head5->next = new Node();
  head5->next->data = 5;
  head5->next->next = new Node();
  head5->next->next->data = 9;
  head5->next->next->next = new Node();
  head5->next->next->next->data = 1;
  head5->next->next->next->next = new Node();
  head5->next->next->next->next->data = 12;
  head5->next->next->next->next->next = NULL;
  printList(head5);

  return 0;
}
