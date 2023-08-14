# Programming-1-Introduction-to-Programming-Friendship-network
Tampere University, Projects made in the course Programming 1: Introduction to Programming

Program Description

In this project you will be implementing a little helpoer program which allows you to analyze the dynamics related to human relationships.

When the program starts is asks the user to enter the name of a file which must contain a textual representation of a friendship network. Next the program reads this file and stores the network information in a suitable data structure to be used later in the program when manipulating the network. Reading and parsing the network file is fulle implemented in the code template you must use to finish this project. Your job however is to choose and implement a suitable data structure and operations to store and manipulate the friendship network data.

After the input file has been read and stored into the data structure you have chosen the code template automatically starts a simple user interface. The user of the program can interact with the date structure using the commands offered by the interface. As it was with the input file reading the user interface is also fully implemented and only requires you to implement the functions which actually search and modify the friendship network data structure.

User Interface Commands

There is already a code template. You only need to extend the template on the locations which are explained with a comment TODO. The comment also explains what you are expected to do in each of these places.

The ready implemented user interface recognizes the commands listed below. All you need to do is to implement the functions the user interface calls to get its job done.

Also, one extra note. Whenever the user interface expects the user to input the next command it prints the following three lines:

Enter one of the commands [Pp]rint/[Aa]dd/[Ff]riends/[Cc]ommon/[Qq]uit

followed by one or more names if needed.

Enter command:

Just by looking at the first it might seem like the commands the user must input are formed by two letters. For example one might think that to print the friendship network one is expected to to type Pp. This is not the case. The bracketed characters mean that any of them can be used to run a command. In other words the print command can be run either by typing lower case p or upper case P. It is probably educating to check the code template to see how this is implemented.

Here are the short descriptions of the commands:

P (Print)

The command will print in alphabetical order all the names in the friendship network. Under each name that person's friends are printed also in alphabetical order. In front of each friend the text "- " is added to make the printout easier to understand. Example printout:

Enter one of the commands [Pp]rint/[Aa]dd/[Ff]riends/[Cc]ommon/[Qq]uit

followed by one or more names if needed.

Enter command: P

MrKrabs

- SpongeBob

Patrick

- Sandy

- SpongeBob

Sandy

- Patrick

- SpongeBob

SpongeBob

- MrKrabs

- Patrick

- Sandy

- Squidward

Squidward

- SpongeBob

A (Add)

After the command letter A (or a) there must be at least names separated by whitespaces. The first of these names will have all the rest added as his or her friend. For example:

Enter one of the commands [Pp]rint/[Aa]dd/[Ff]riends/[Cc]ommon/[Qq]uit

followed by one or more names if needed.

Enter command: A Rick Morty Summer

will result the friendships Rick–Morty, Morty–Rick, Rick–Summer, and Summer–Rick to be added into the network.

Please not that "A" command can be used to add new friendships into a network which was originally initialized by the information read from the input file.

F (Friends)

This command will print in alphabetical order all the friends of the person whose name was given after the command character. For example:

Enter one of the commands [Pp]rint/[Aa]dd/[Ff]riends/[Cc]ommon/[Qq]uit

followed by one or more names if needed.

Enter command: F Anna

Brutus

Celia

Erin

Florian

James

C (Common friends)

After the C command one must be followed by two names. Commond friends of these two persons will be printed on the screen in alphabetical order. Common friends are people who are friends with both of the persons whose names the user typed after the command character. If those two people don't have common friends a message will be printed as shown in the following example:

Enter one of the commands [Pp]rint/[Aa]dd/[Ff]riends/[Cc]ommon/[Qq]uit

followed by one or more names if needed.

Enter command: C Anna Florian

Brutus

James

Enter one of the commands [Pp]rint/[Aa]dd/[Ff]riends/[Cc]ommon/[Qq]uit

followed by one or more names if needed.

Enter command: C Florian Anna

Brutus

James

Enter one of the commands [Pp]rint/[Aa]dd/[Ff]riends/[Cc]ommon/[Qq]uit

followed by one or more names if needed.

Enter command: C Helen Nina

Helen and Nina have no common friends.

Q (Quit)

The program ends:

Enter one of the commands [Pp]rint/[Aa]dd/[Ff]riends/[Cc]ommon/[Qq]uit

followed by one or more names if needed.

Enter command: Q

Farewell cruel world...

Errors

Handling the error conditions are explained in the code template and you should follow the instructions given there.

Example execution

The following example presumes that the input file which was used is friendships.txt corresponds to the image given earlier in this document.


Enter the name of the input file: friendships.txt

File friendships.txt successfully read.

Enter one of the commands [Pp]rint/[Aa]dd/[Ff]riends/[Cc]ommon/[Qq]uit

followed by one or more names if needed.

Enter command: P

Anna

- Brutus

- Celia

- Erin

- Florian

- James

Brutus

- Anna

- Celia

- Florian

Celia

- Anna

- Brutus

- David

David

- Celia

- Erin

Erin

- Anna

- David

- Irina

- James

Florian

- Anna

- Brutus

- Greta

- Helen

- Irina

- James

Greta

- Florian

- Helen

- Irina

Helen

- Florian

- Greta

- Irina

Irina

- Erin

- Florian

- Greta

- Helen

- James

James

- Anna

- Erin

- Florian

- Irina

Kira

- Lucius

- Mia

Lucius

- Kira

- Mia

- Nina

Mia

- Kira

- Lucius

- Nina

Nina

- Lucius

- Mia

Enter one of the commands [Pp]rint/[Aa]dd/[Ff]riends/[Cc]ommon/[Qq]uit

followed by one or more names if needed.

Enter command: F Kira

Lucius

Mia

Enter one of the commands [Pp]rint/[Aa]dd/[Ff]riends/[Cc]ommon/[Qq]uit

followed by one or more names if needed.

Enter command: A Kira Samantha

Enter one of the commands [Pp]rint/[Aa]dd/[Ff]riends/[Cc]ommon/[Qq]uit

followed by one or more names if needed.

Enter command: F Kira

Lucius

Mia

Samantha

Enter one of the commands [Pp]rint/[Aa]dd/[Ff]riends/[Cc]ommon/[Qq]uit

followed by one or more names if needed.

Enter command: F Samantha

Kira

Enter one of the commands [Pp]rint/[Aa]dd/[Ff]riends/[Cc]ommon/[Qq]uit

followed by one or more names if needed.

Enter command: C Erin Celia

Anna

David

Enter one of the commands [Pp]rint/[Aa]dd/[Ff]riends/[Cc]ommon/[Qq]uit

followed by one or more names if needed.

Enter command: C Celia Erin

Anna

David

Enter one of the commands [Pp]rint/[Aa]dd/[Ff]riends/[Cc]ommon/[Qq]uit

followed by one or more names if needed.

Enter command: C Irina Lucius

Irina and Lucius have no common friends.

Enter one of the commands [Pp]rint/[Aa]dd/[Ff]riends/[Cc]ommon/[Qq]uit

followed by one or more names if needed.

Enter command: A Sam Dean

Enter one of the commands [Pp]rint/[Aa]dd/[Ff]riends/[Cc]ommon/[Qq]uit

followed by one or more names if needed.

Enter command: C Sam Dean

Sam and Dean have no common friends.

Enter one of the commands [Pp]rint/[Aa]dd/[Ff]riends/[Cc]ommon/[Qq]uit

followed by one or more names if needed.

Enter command: F Sam

Dean

Enter one of the commands [Pp]rint/[Aa]dd/[Ff]riends/[Cc]ommon/[Qq]uit

followed by one or more names if needed.

Enter command: F Dean

Sam

Enter one of the commands [Pp]rint/[Aa]dd/[Ff]riends/[Cc]ommon/[Qq]uit

followed by one or more names if needed.

Enter command: Q

Farewell cruel world...
