* Example with code to show state and behaviour of an object where behaviour depends upon the state of object?
* What is the definition of hashcode as per java 8 document?
* What is the fully qualified name of Object class in java ?
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
        Test t1 = t;
        System.out.println(t1 == t);
        t1.x = 300;
        t1.y = "alex";
        System.out.println(t.x);
        System.out.println(t.y);
    }
}

```
* Identify State & Behaviour. Find where the state is used. Does behavour depends on the state?
```java
public class Calculator
{
   private int i;
   private int j;
   
   public Calculator(int i, int j)
   {
     this.i = i;
     this.j = j;
   }
   
   public int sum()
   {
     return i + j;
   }
}
```
* Find the output? Identify the static method & variables.
```
public class Test
{
  static int x;
  int y;
  static{
    x = 10;
  }
  
  static{
    x = x + 20;
  }
  
  {
    y = 100;
  }
  
  {
    y = y + 20;
  }
  
  public static void main(String[] args)
  {
    Test t = null;
    t.x = t.x + 40;
    x = x + 50;
    
    t = new Test();
    t.y = t.y + 200;
    
    Test t1 = new Test();
    System.out.println(t.x)
    System.out.println(t1.x)
    System.out.println(Test.x)
    
    System.out.println(t.y)
    System.out.println(t1.y)
   
   System.out.println(t.getX());
   System.out.println(t1.getX());
   System.out.println(Test.getX());
   
   System.out.println(t.getSum());
   System.out.println(t1.getSum());
   
  }
  
  public static int getX()
  {
    return x;
  }
  
  public static int getSum()
  {
    return  x + y;
  }
}

