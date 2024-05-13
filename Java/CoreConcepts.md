# Interface in java
In interface you can only use public access modifier.NO Private or protected.

```
public interface Phone {
    String processor();
    String OS();
    int spaceInGB();
}
```

```
public class Iphone8 implements Phone{
    @Override
    public String processor() {
        return "A11";
    }

    @Override
    public String OS() {
        return "IOS";
    }

    @Override
    public int spaceInGB() {
        return 64;
    }
}
```

```
public class OnePlus5 implements Phone{
    @Override
    public String processor() {
        return "SD835";
    }

    @Override
    public String OS() {
        return "Android";
    }

    @Override
    public int spaceInGB() {
        return 64;
    }
}
```

```
public static void main(String[] args) {
    Phone phone = new OnePlus5();
    System.out.println("Processor: " + phone.processor());
    System.out.println("Space in GB: " + phone.spaceInGB());
}

```

# Output:
```
Processor: SD835
Space in GB: 64
```
