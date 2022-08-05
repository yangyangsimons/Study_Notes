#### 1. we use ObjectOutputStream to serialize an object, but when we change the class file which the object belongs to, there will be a `InvalidClassException`;

Thrown when the Serialization runtime detects one of the following problems with a Class.
1. The serial version of the class does not match that of the class descriptor read from the stream.
2. The class contains unknown datatypes.
3. The class does not have an accessible no-arg constructor.

How to fix this exception?
Give the class a fixed serivalVersionUID.
`private static final long servialVersionUID = 41L;`

#### 2. If we do not want serialize one of the property of the class, use `transient`.
`private transient int age;`

