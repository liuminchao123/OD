知识点

* Integer.parseInt(string, int);  将字符串按照对应的进制进行转换

```java
import java.io.*;
import java.util.*;

public class Main{
    public static void main(String[] args) throws Exception{
        Scanner sc = new Scanner(System.in);
        while(sc.hasNextLine()){
            String s = sc.nextLine();
          	System.out.println(
              Integer.parseInt(s.substring(2,s.length()),16));
        }
    }
}
```

