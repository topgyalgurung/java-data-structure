# Java Built in Data Structures Guided Project

### Read weather data from a file and populate a Java ArrayList with the file data. The data is then uniquified in a Set data structure and stored in a HashMap for accessing data by year.

#### Java's collections framework contains data structures that are built for efficiency
 - A list such as an ArrayList can be used in place of an array to contain data where the size cannot be determined ahead of time.
 -  A LinkedList is like an ArrayList, except elements can be more quickly added and deleted from it, since no shifting needs to occur. 
 -  A Hashmap is used to quickly look up a value based on a key rather than a numerical index
-  A Set may be used to remove duplicates from a list, simply by assigning the data to it.


Task Steps:
1. Analyze the existing application and create a Java ArrayList to populate with data from a file.
    * Replace array code with arraylist code. 
    * arraylist grows with data size
    * uses add method to add elements
        - Advantage of using arraylist is we dont have to know the size of the file ahead of the time. 

1. Create and Populate a Java LinkedList with the data and compare its performance with ArrayList.
    * linkedlist contains nodes. each node contains a reference to previous object and next object memory is not contiguous like arraylist
    * removal, addition from/ to the list is more efficient
    * List can be arraylist, linkedlist. This is polymorphism can take many forms .
        - Linkedlist takes less time because we do not have to shift the array. Set of nodes in linkedlist distributed across memory not contiguous.

2. Use a Set data structure to uniquify the data from the LinkedList.
    * Set removes duplicate entries
    * Set is a reference type. Implementation is HashSet
    * Output the HashSet to check the data
      -  To remove duplicate, we need to implement equals method in YearAvg java. After toCSV(), right click, then source action, then Generate hashCode() and equals(). we need equals method to check if two object are equal or not 

3. Sort the Set data according to rain and store it in a file.
    * Change the HashSet to a TreeSet
    * Data is sorted automatically
    * CompareTo method in the YearAvg class is used
    * Store the Set to the File
        - When we have Comparable interface, we also need to implement method like compareTo.
 
4. Create a HashMap of the data and look up a record based on a unique key.
    * Use the Hashmap to look up the data by year
    * populate the hashmap in the file read loop
    * check that the key exists
    * retrieve the temp, rainfall avg. data based on the key

