### Denial Of service

## exploit 1 : quit the server
Any user can take down the server by visiting the /quitserver url

## Fix
Simply correct the Protected urls as, it only contained "/quit" and not "/quitserver"


## exploit 2 : RESET the server
Any user could take down the server by visiting the /RESET url (as the check :is not case sensitive)

## Fixed with the implemented pathTraversal defense (case sensitive)




## exploit 3 : Overloading the Server 

## Fixed as the path traversal attacks are required and already fixed

