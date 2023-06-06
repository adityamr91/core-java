

**Transient**
 transient is a keyword that is used to indicate that a field or variable should not be serialized
 there may be certain fields that should not be included in the serialization process
 For example, if a class has a field that contains sensitive information, such as a password
 
 **Volatile**
 volatile keyword is used to indicate that a variable's value may be modified by multiple threads
 changes are made in main memory directly, no local temp chache memory is involved
 Java Memory Model ensures that any changes made to the variable by one thread are immediately visible to all other threads that access the variable
 
 **Atomic**
 an atomic variable is a variable that can be updated atomically, meaning that it is updated in a single, indivisible operation. This is important in multi-threaded applications, where multiple threads may be accessing and modifying the same variable at the same time.
 
 The java.util.concurrent.atomic package provides a set of classes for working with atomic variables, including AtomicInteger, AtomicLong, and AtomicBoolean. These classes provide methods for performing atomic operations, such as incrementing and decrementing a value, setting a value, and getting and setting values atomically.
 
 **Shallow Copy**
 A shallow copy creates a new object that references the same memory locations as the original object. Any changes made to the new object will also be reflected in the original object. 
 ```
 String[] name = {"John"};
Person person1 = new Person(name);
Person person2 = person1.shallowCopy();

System.out.println(Arrays.toString(person1.getName())); // prints "[John]"
System.out.println(Arrays.toString(person2.getName())); // prints "[John]"

name[0] = "Jane";

System.out.println(Arrays.toString(person1.getName())); // prints "[Jane]"
System.out.println(Arrays.toString(person2.getName())); // prints "[Jane]"
 ```
 
 **Deep Copy**
 A deep copy creates a new object that is a copy of the original object, but with its own memory locations. Any changes made to the new object will not be reflected in the original object.
 ```
 Person person1 = new Person("John");
Person person2 = person1.deepCopy();

System.out.println(person1.getName()); // prints "John"
System.out.println(person2.getName()); // prints "John"

person1.setName("Jane");

System.out.println(person1.getName()); // prints "Jane"
System.out.println(person2.getName()); // prints "John"

 ```
**Fail-Fast Iterator**
A fail-fast iterator is an iterator that throws a ConcurrentModificationException if the collection is modified while the iterator is traversing it. This is because the iterator is designed to detect any modifications made to the collection while it is being traversed.

the default iterator implementation for ArrayList, HashSet, and HashMap is fail-fast.

**Fail-Safe Iterator**
A fail-safe iterator is an iterator that does not throw a ConcurrentModificationException if the collection is modified while the iterator is traversing it. Instead, a copy of the collection is made and the iterator traverses the copy. This means that the iterator will not see any changes made to the original collection.

if you want to use a fail-safe iterator, you can use the CopyOnWriteArrayList, CopyOnWriteArraySet, and ConcurrentHashMap classes. These classes create a copy of the collection when it is modified, so the iterator can continue to traverse the original collection without seeing any modifications.

It is important to note that fail-safe iterators can be slower and use more memory than fail-fast iterators, as a copy of the collection is made. However, fail-fast iterators can be more efficient if the collection is modified infrequently or if the modifications are small.
