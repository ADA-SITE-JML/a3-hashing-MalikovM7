Option B
I wrote the code in C# language because I have more experience with that and familiar with its syntax.
I used SHA256 internal C# Cryptography hash library (I could not install xxHash or any external hash libraries).
To run this code, you should add command line arguments for n and s values. In JetBrains Rider: Run->Edit Configurations->Program Arguments.

How the program works: when you write a string it first hashes it then stores hashcode into bucket which index was also calculated in the code. When the number of characters in the bucket exceeds s, it creates first overflow bucket and calls it (f.e 3_overflow1.txt), after when you add one more string in the same bucket it makes (3_overflow2.txt) and that continues. 

All logs:

24 March: It is my first log, here I want to explain where I will write my code and what hashing technique I will use. I will write a console app on C# .NET 6.0, and will use SHA256 hashing function which is built in.

28 March: Created a console app and added User input readline in main method, to get n and s values which represent the number of buckets and the amount of records which the bucket can contain.

2 April: wrote main hash function method which computes a hash of the input string using SHA256 algorithm.

4th april: I have seen your comments in discussions, You asked to run the program with console arguments that is why I changed the part when I first was asking from user n and s values and added them directly from run configurations.
also I wrote a method for creating next overflow file and writing into the bucket , where I considered that comma ',' is dividing the strings

5th April: Final version of code with the comments of explanation of every line. Added writing to bucket method while loop which controls all operations from hashing and storing into buckets by calling those methods in it.

