* Example with code to show state and behaviour of an object where behaviour depends upon the state of object?
* What is the definition of hashcode as per java 8 document?
* What is the full qualified name of Object class in java ?
* Object class is in which package ?
* Note : Find the output? Always write the explanation for the output. why you are getting that output?
* Find the output?
```java
public class Test
{
  public static void main(String[] args)
  {
    Object obj1 = new Object();
    Object obj2 = new Object();
    System.out.println(obj1.hashCode() == obj2.hashCode());
    System.out.println(obj1.getClass());
    System.out.println(obj1 == obj2);
  }
}
```
* Find the output?
```java
public class Test {
    int x;
    public Test(int x){
        this.x = x;
    }
    public static void main(String[] args) {
        Test t = new Test(10);
        System.out.println(t.x);
    }
}
```
* Why below code will not compile? What is the fix we have to do so that the code will compile.
```java
public class Test {
    int x;
    public Test(int x){
        this.x = x;
    }
    public static void main(String[] args) {
        Test t = new Test();
        System.out.println(t.x);
    }
}
```
* Will below code will compile?
```java
public class Test {
    int x;
    public Test(int x){
        this.x = x;
    }
    public Test()
    {
        
    }
    public static void main(String[] args) {
        Test t = new Test();
        System.out.println(t.x);
    }
}
```
* Find the output?
```java
public class Test {
    int x;
    String y;
    public static void main(String[] args) {
        Test t = new Test();
        System.out.println(t.x);
        System.out.println(t.y);
    }
}
```
* What is the default value of int , String variables ?
* Find the output?
```java
public class Test {
    int x;
    String y;

    public Test(int x, String y) {
        this.x = x;
        this.y = y;
        Test tVar = this;
        System.out.println(tVar.hashCode() == this.hashCode());
    }

    public static void main(String[] args) {
        Test t = new Test(10,"john");
        System.out.println(t.x);
        System.out.println(t.y);
    }
}
```
* Find the output?
```java

public class Test {
    int x;
    String y;

    public Test(int x, String y) {
        this.x = x;
        this.y = y;
        m1(this);
    }

    public static void main(String[] args) {
        Test t = new Test(10,"john");
        System.out.println(t.x);
        System.out.println(t.y);
    }
    
    public void m1(Test t1)
    {
        t1.x = 100;
        t1.y = "Doe";
    }
}
```
* Find the output? 
```java

public class Test {
    int x;
    String y;

    public Test(int x, String y) {
        this.x = x;
        this.y = y;
        this.m1(this);
    }

    public static void main(String[] args) {
        Test t = new Test(10,"john");
        System.out.println(t.x == 10);
        System.out.println(t.y == "john");
    }

    public void m1(Test t1)
    {
        t1.x = 100;
        t1.y = "Doe";
    }
}
```
* Find the output?
```java
public class Test {
    int x;
    String y;

    public Test(int x, String y) {
        x = x;
        y = y;
        this.m1(this);
    }

    public static void main(String[] args) {
        Test t = new Test(10,"john");
        System.out.println(t.x);
        System.out.println(t.y);
    }

    public void m1(Test t1)
    {
        t1.x = 100;
        t1.y = "Doe";
    }
}
```
* Find the output?
```java
public class Test {
    int x;
    String y;

    public Test(int x, String y) {
        x = x;
        y = y;
    }

    public static void main(String[] args) {
        Test t = new Test(10,"john");
        System.out.println(t.x);
        System.out.println(t.y);
    }

    public void m1(Test t1)
    {
        t1.x = 100;
        t1.y = "Doe";
    }
}
```
