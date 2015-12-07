# Android-SDK-SQLInjection
SQL Injection found in Android's Internal API, `SQLiteDatabase` class.

The bug is quite simple to understand, i looked at the internal source of `SQLiteDatabase.replace()` function, which is `insertWithOnConflict()` that should be protected to sql injection attacks and i found that the column name is being concatenated without any validation from the hashtable. which can lead (by an insecure usage of the function to SQL Injection attacks on applications).
**Note: The whole class is vulnerable to this attack. this function is given as an example.
# Screenshot
![alt tag](http://s23.postimg.org/q4og9dh0b/androidsqlinj.png)
