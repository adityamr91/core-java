# Collection

**ArrayList**
1. Fast in indexing, slow in add & delete when compared to LinkedList
2. duplicates allowed, Null allowed
3. Not Thread Safe
4. Inmplements RandomAccess and Colneable Interfaces

**Vector**
1. same as ArrayList but ThreadSafe

**LinkedList**
1. Fast in add & delete, slow inindexing when compared to ArrayList
2. duplicates allowed, Null allowed

**HashSet**
1. duplicates not allowed & insertion ordered not maintained

**TreeSet**
1. customized sorting order allowed, duplicates not allowed

**HashMap**
1. key value pair insertion
2. duplicate keys not allowed, one null key allowed
3. duplicate values allowed 
4. not thread safe

**TreeMap**
1. key value pair insertion based on keys sorting

**HashTable**
1. no duplicates, no null value allowed
2. thread safe

**1. default size, increment factor and constructors**

| Collection | ArraList  | LinkedList | Vector | 
| ------------- | ------------- | ------------- | ------------- | 
| **Default Size** | 10  | N/A  | 10  | 
| **Default Increment** | +10 ((Current capacity*3/2)+1)  | N/A  | +10 (Current capacity * 2)  | 
| **Constructors** | 1. ArrayList()                    | 1. LinkedList()             | 1. Vector()                      | 
|                 | 2. ArrayList(Collection c)        | 2. LinkedList(Collection c) | 2. Vector(int initialCapacity)   | 
|                 | 3. ArrayList(int initialCapacity) | -                        | 3. Vector(int capacityIncrement) | 
|                 | 4. ArrayList(E[] array)           | -                        | 4. Vector(int initialCapacity, int capacityIncrement)  | 
|                 |           -                    | -                        | 5. Vector(Collection c)          | 


| Collection | HashSet | TreeSet | 
| ------------- | ------------- | ------------- | 
| **Default Size** | 16  | 0  | 
| **Default Increment** | + (x 0.75)  | N/A  | 
| **Constructors** | 1. HashSet()  | 1. TreeSet()  |
|| 2. HashSet(Collection c)  | 2. TreeSet(Comparator comparator)  | 
|| 3. HashSet(int initialCapacity, float loadFactor)  | 3. TreeSet(Collection c)  | 
|| -  | 4. TreeSet(SortedSet s)  | 
|| - | 5. TreeSet(E[] a) | 


| Collection | HashMap | TreeMap | HashTable |
| ------------- | ------------- | ------------- | ------------- |
| **Default Size** | 16  | 16  | 16  |
| **Default Increment** | + (x 0.75)    | +16  | + (x 0.75)  |
| **Constructors** |  1. HashMap()  | 1. TreeMap()  | 1. Hashtable()  |
|| 2. HashMap(int initialCapacity)  | 2. TreeMap(Comparator comparator)  | 2. Hashtable(int initialCapacity)  |
|| 3. HashMap(int initialCapacity, float loadFactor)  | 3. TreeMap(Map map)  | 3. Hashtable(int initialCapacity, float loadFactor)  |
|| 4. HashMap(Map m)  | 4. TreeMap(SortedMap map)  | 4. Hashtable(Map m)  |
|| 5. HashMap(int initialCapacity, float loadFactor, boolean accessOrder):   | 5. TreeMap(Collection c, Comparator comparator)  | -  |

| HashMap         | HashTable     | ConcurrentHashMap |
| -------------   | ------------- | -------------     |
| Not Thread Safe | Thread Safe   | Thread Safe       |
|                 |  Single Object Lock | 16 Object Lock (Default Cunccurency Level = 16 |
|                 |               | basically object is divided into 16 segments  |













