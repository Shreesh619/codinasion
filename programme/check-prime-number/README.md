## Write a program to check prime number

```
Input  : 7
Output : Prime number
```

---

<CodeBlock slots="heading, code" repeat="2" languages="Python, Java" />

#### Python

```python
# check prime number function
def check_prime(num):
    if (num == 0 or num == 1):
        return "Not prime number"
    for i in range(2, num//2+1):
        if num % i == 0:
            return "Not prime number"
    return "Prime number"

# programme driver
n = int(input("Input : "))
print("Output :", check_prime(n))
```

#### Java

```java
import java.util.*;

public class solution {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.print("\nInput: ");
        int n = sc.nextInt();

        if (n == 0 || n == 1) {
            System.out.println("Output: Not prime number");
        } else {
            int temp = 0;
            for (int i = 2; i < n / 2; i++) {
                if (n % i == 0) {
                    temp = 1;
                    break;
                }
            }

            if (temp == 1) {
                System.out.println("Output: Not prime number");
            } else {
                System.out.println("Output: Prime number");
            }
        }
        sc.close();
    }
}
```
