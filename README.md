24 March: It is my first log, here I want to explain where I will write my code and what hashing technique I will use. I will write a console app on C# .NET 6.0, and will use SHA256 hashing function which is built in.
28 March: Created a console app and added User input readline in main method, to get n and s values which represent the number of buckets and the amount of records which the bucket can contain.
2 April: wrote main hash function method which computes a hash of the input string using SHA256 algorithm.

How hashing (SHA256) algorithm works?

byte[] hashBytes = sha256.ComputeHash(Encoding.UTF8.GetBytes(input));
in this line it converts the input string to bytes, and using sha256.ComputeHash it hashes the byte array.

int hashInt = BitConverter.ToInt32(hashBytes, 0);
in this line it takes first 4 bytes and converts them to integers, it is needed because we need the number not the full hashcode.

return (Math.Abs(hashInt) % bucketCount) + 1;
this line makes us sure that the result is non negative and fits into the range of buckets from 1 to n.


