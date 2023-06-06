

**Transient**
 transient is a keyword that is used to indicate that a field or variable should not be serialized
 there may be certain fields that should not be included in the serialization process
 For example, if a class has a field that contains sensitive information, such as a password
 
 **Volatile**
 volatile keyword is used to indicate that a variable's value may be modified by multiple threads
 changes are made in main memory directly, no local temp chache memory is involved
 Java Memory Model ensures that any changes made to the variable by one thread are immediately visible to all other threads that access the variable
 
 **atomic**
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

