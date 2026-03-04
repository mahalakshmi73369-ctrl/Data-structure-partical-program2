class Node:
    def __init__(self, sid, name, marks):
        self.sid = sid
        self.name = name
        self.marks = marks
        self.next = None

head = None

def insert_end():
    global head
    sid = input("Enter ID: ")
    name = raw_input("Enter Name: ")
    marks = input("Enter Marks: ")
    new = Node(sid, name, marks)
    if head is None:
        head = new
    else:
        temp = head
        while temp.next:
            temp = temp.next
        temp.next = new

def display():
    temp = head
    while temp:
        print temp.sid, temp.name, temp.marks
        temp = temp.next# Data-structure-partical-program2
