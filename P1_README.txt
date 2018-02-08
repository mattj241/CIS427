CIS 427 - Winter 2018 - Program 1

Group: Matthew London , Daniil Shmerko

Responsibilities:
All work was very evenly split. 
 - Daniil implemented the basis for starting the project/the overall design, along with code refactoring, commenting, and superb error handling.
 - Matthew implemented the commands, error handling, file read/writing, and this README.

Implemented Commands:
ADD - format: add <first name> <last name> <phone # (ex. 734-880-9921)>
DELETE - format: delete <log ID>
LIST - format: list
QUIT - format: quit
SHUTDOWN - format: shutdown

How to compile and run this project:
1) You must have 2 instances of the UNIX terminal windows under the UMD servers. 1 for the server, and 1 for the client. 
  Unpack the .tar file in a destination you please, all the files should remain in the same directory.

2) In 1 UNIX terminal, type exactly whats in the quotes: "javac Server.java" and "javac Client.java" in the other UNIX terminal.

3) In the server terminal, type "java Server" to start running the server. A newline should be shown in the server terminal.

4) In the client terminal, type "java Client" to initiate a connection to the running server. "Usage: <Server IP Address>" should appear in the client terminal.
   Type "127.0.0.1" and press enter in the client terminal. If done correctly, a response from both the client and server will appear to verify a successful connection.

5) Go ahead and test any commands.

Known Bugs:
N/A, hopefully you don't prove us wrong!

Sample Client runs:
ADD	
 - input: add Matt London 734-000-1010
 - client: 200 OK
	   The new record is: 1001
 - server: 200 OK Adding listing to log...

DELETE
 - input: delete 1000
 - client: 403 The Record ID does not exist.
 - server: ID not found.

 - input: delete 1001
 - client: 200 OK
 - server: 200 OK Removing listing from log...

LIST
 - input: list
 - client: Empty Log!
 - server: 200 OK Listing log to client...

 - input: list
 - client: (Sample log book!)
	1002 Matt London 111-111-1111
	1003 Jin Guo 111-111-1112
	1004 Mo Van 111-111-1113
	1005 Bruce Elenbogen 111-111-1114
	1006 Hello World 111-111-1115
 - server: 200 OK Listing log to client...

QUIT
 - input: quit
 - client: 200 OK
 - server: 200 OK Client connection removed.

SHUTDOWN
 - input: shutdown
 - client: 200 OK
 - server: 200 OK SHUTDOWN
	   Shutting down...writing log to memory file.