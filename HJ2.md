知识点

* split 分割输入的字符串
* charAt() 获取字符串第几个字符
* （byte)获得对应的阿斯克码
* Objects.equals(word2, str.charAt(0))  牛客网无法通过编译
* next获得一个字符
* nextLine获得一行字符串



代码

```java
import java.util.Objects;
import java.util.Scanner;

// 注意类名必须为 Main, 不要有任何 package xxx 信息
public class Main {
    public static void main(String[] args) {
        char word1;
        char word2;
        int num;
        int i = 0;
        Scanner sc = new Scanner(System.in);
        String[] array = sc.nextLine().split("");
        word1 = sc.next().charAt(0);
        num = (byte)word1;
        // 先遍历一次
        for (String str : array) {
            if (Objects.equals(word1, str.charAt(0)))
                i++;
        }
        if(num >= 65 && num <= 90) {
            word2 = (char)(word1 + 32);
            for (String str : array) {
                if (Objects.equals(word2, str.charAt(0)))
                    i++;
            }
        }
        if(num >= 97 && num <= 122){
            word2 = (char)(word1 - 32);
            for (String str : array) {
                if (Objects.equals(word2, str.charAt(0)))
                    i++;
            }
        }
        System.out.println(i);
    }
}
```



