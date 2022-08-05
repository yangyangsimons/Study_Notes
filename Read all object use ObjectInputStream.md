when we use the ObjectInputStream to store a lot of objects in a file, and the problem is how to use method`readObject()` get all the objects from this file, since there are no `readall()` method provide by ObjectInputStream. Below code can help;
```java
ObjectIntputStream ois = new ObjectInputStream("/test.txt");
ArrayList<Student> al = new ArrayList<>();
try{
  while(true){
    Student s = (Student) ois.readObject(); 
    al.add(s);
  }
}catch(EOFException e){
  e.printStackTrace();
}
for(Student s : al){
  System.out.println(s.getName()+"," + s.getAge())
}

```
