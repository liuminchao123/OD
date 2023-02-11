知识点

* substring 截取一段字符串

* next() 与 nextLine() 区别

  next():

  一定要读取到有效字符后才可以结束输入。
  对输入有效字符之前遇到的空白，next() 方法会自动将其去掉。
  只有输入有效字符后才将其后面输入的空白作为分隔符或者结束符。
  next() 不能得到带有空格的字符串。

  nextLine()：

  以Enter为结束符,也就是说 nextLine()方法返回的是输入回车之前的所有字符。
  可以获得空白。

* hasNext() 与 hasNextLine() 区别

  hasNext():

  1、输出为布尔值
  2、判断输入的缓存中是否有效字符，遇到空格结束。
  3、如果只输入空格，不会匹配，阻塞，不会返回false

  hasNextLine()：

  1、以Enter为结束符，判断此行有没有输入，空白输入也会返回true

* 没有line的 next, hasnext 遇到空格就结束

* 有line的，遇到回车才结束



```java
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        while(input.hasNextLine()){  // 输入一行，输出一行
            String s = input.nextLine();  // 存储字符串
            split(s);
        }
    }

    public static void split(String s){
        while(s.length()>=8){
            System.out.println(s.substring(0,8)); // 截取输出
            s=s.substring(8);  // 让字符串不断变小
        }
        if(s.length()<8 && s.length()>0){
            s+="00000000";
            System.out.println(s.substring(0,8));
        }
    }
}
```