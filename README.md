This is a programmed example of a linked list used for a simple task such as a task manager / to-do list. The list uses a
struct to designate a node and has functons surrounding it to dynamically add or remove tasks. Tasks can be added at the
beginning or the end of the list and will be assigned a priority number. The program gives the user a terminal menu to access
the linked list with 5 options not including the closing of the programm.

Option 1, Add Task at Begining: 
The function requires a string formmated description for the task and an interger priority (ie. 3, 1, or 4). 
It will create a new node and connenct it to the previous head of the linked list. This new node becomes the new head and 
the list is returned. There is no need to check if the list is empty as a new head will always be assigned. 

Option 2, Add Task at End:
This function requires the head node to be passed along with a string formatted description and an interger priority. First it
will dynamically add a node using "new" and passing it the given information. Next, it will check to see if the current head is a 
null pointer. If true, the new node will become the new head. Otherwise, the program will follow the links bewteen each node until
it reaches a null pointer / the tail node. It will the connect the tail node to the new node, making it the new tail node. It will
then return the head node because the head node has not changed.

Option 3, View All Tasks:
This function only requires a head node to be passed. First it will check if the head is a null pointer. If true, it will print that
there are no tasks to display because the list is empty. Otherwise, It will contiuously print out the tasks in the list while traversing
each node in the list with its position and priority. This will end once it has reached a null pointer / the end of the list.

Option 4, Search for Task Description:
The function needs to be passed the head node and a string formmatted decription. It will then enter a loop that will continue until it
reaches the end of the list. During each iteration, the program will add 1 to the current position so the user can see the index number 
of the task. It wil also check if the current node's description matches the input description. If true, it will print that the task
has been found and its index number and close the function. If false, it will move on to the next node in the list and repeat the loop.
If the loop reaches the end of the list without finding a match, it will print that the task has not been found.

Option 5, Delete Task at Position:
This function requires the head node and an integer position / index of the requested task to delete. First it checks to see if the index
is 1. If true, this means that the head will be deleted and the next node in the list will become the new head. Otherwise it will enter a
loop that wil continue until the list is empty or the node before the position has been reached. Once the loop has stopped, it will check
to see if the current or next node is a null pointer. If true, it will print that the position is invalid as that node index number 
doesn't exist. If false, It will connect the current node to point to the node after the next node thus removing it from the list.
It then delets that node and returns the head node.
