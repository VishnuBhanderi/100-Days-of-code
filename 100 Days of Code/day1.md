# Day 1
## Number of Problems Solved: 4

### Problem #1 [Roller Coaster](https://www.codechef.com/START37D/problems/MINHEIGHT)
#### 

#### Related Topics:
Math
#### Code:
```java


import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;
import java.lang.Math;
import java.util.Scanner;
import java.io.*;
import java.util.*;
import java.util.StringTokenizer;

public class Main {
   static class FastReader {
      BufferedReader br;
      StringTokenizer st;

      public FastReader() {
         br = new BufferedReader(new InputStreamReader(System.in));
      }

      String next() {
         while (st == null || !st.hasMoreElements()) {
            try {
               st = new StringTokenizer(br.readLine());
            } catch (IOException e) {
               e.printStackTrace();
            }
         }
         return st.nextToken();
      }

      int nextInt() {
         return Integer.parseInt(next());
      }

      long nextLong() {
         return Long.parseLong(next());
      }

      double nextDouble() {
         return Double.parseDouble(next());
      }

      String nextLine() {
         String str = "";
         try {
            str = br.readLine();
         } catch (IOException e) {
            e.printStackTrace();
         }
         return str;
      }
   }

   static int countSC(int N) {
      int res = (int) Math.sqrt(N) +
            (int) Math.cbrt(N) -
            (int) (Math.sqrt(Math.cbrt(N)));

      return res;
   }

   public static void main(String[] args) throws Exception {
      // TODO Auto-generated method stub
      FastReader sc = new FastReader();
      BufferedWriter ou = new BufferedWriter(new OutputStreamWriter(System.out));
      // Start coding

      int n = sc.nextInt();

      for (int i = 0; i < n; i++) {
         int x = sc.nextInt();
         int h = sc.nextInt();

         if (x >= h) {
            ou.write("YES" + "\n");
         }

         else {
            ou.write("NO" + "\n");
         }
      }
      ou.flush();
   }
}

```
#### Time Taken: 2 mins

### Problem #2 [The Mango Truck](https://www.codechef.com/START37D/problems/MANGOES)
#### 

#### Related Topics:

Math

#### Code:
```java
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;
import java.lang.Math;
import java.util.Scanner;
import java.io.*;
import java.util.*;
import java.util.StringTokenizer;

public class Main {
   static class FastReader {
      BufferedReader br;
      StringTokenizer st;

      public FastReader() {
         br = new BufferedReader(new InputStreamReader(System.in));
      }

      String next() {
         while (st == null || !st.hasMoreElements()) {
            try {
               st = new StringTokenizer(br.readLine());
            } catch (IOException e) {
               e.printStackTrace();
            }
         }
         return st.nextToken();
      }

      int nextInt() {
         return Integer.parseInt(next());
      }

      long nextLong() {
         return Long.parseLong(next());
      }

      double nextDouble() {
         return Double.parseDouble(next());
      }

      String nextLine() {
         String str = "";
         try {
            str = br.readLine();
         } catch (IOException e) {
            e.printStackTrace();
         }
         return str;
      }
   }

   static int countSC(int N) {
      int res = (int) Math.sqrt(N) +
            (int) Math.cbrt(N) -
            (int) (Math.sqrt(Math.cbrt(N)));

      return res;
   }

   public static void main(String[] args) throws Exception {
      // TODO Auto-generated method stub
      FastReader sc = new FastReader();
      BufferedWriter ou = new BufferedWriter(new OutputStreamWriter(System.out));
      // Start coding

      int n = sc.nextInt();

      for (int i = 0; i < n; i++) {
         int x = sc.nextInt();
         int y = sc.nextInt();
         int z = sc.nextInt();

         int ans = (z - y) / x;
         ou.write(ans + "\n");
      }
      ou.flush();
   }
}

```
#### Time Taken: 3 min

### Problem #3 [Laptop Recommendation](https://www.codechef.com/START37D/problems/LAPTOPREC) 

#### Related Topics:

Math

#### Code:
```java
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;
import java.lang.Math;
import java.util.*;
import java.io.*;
import java.util.*;
import java.util.StringTokenizer;

public class Main {
   static class FastReader {
      BufferedReader br;
      StringTokenizer st;

      public FastReader() {
         br = new BufferedReader(new InputStreamReader(System.in));
      }

      String next() {
         while (st == null || !st.hasMoreElements()) {
            try {
               st = new StringTokenizer(br.readLine());
            } catch (IOException e) {
               e.printStackTrace();
            }
         }
         return st.nextToken();
      }

      int nextInt() {
         return Integer.parseInt(next());
      }

      long nextLong() {
         return Long.parseLong(next());
      }

      double nextDouble() {
         return Double.parseDouble(next());
      }

      String nextLine() {
         String str = "";
         try {
            str = br.readLine();
         } catch (IOException e) {
            e.printStackTrace();
         }
         return str;
      }
   }

   public static void main(String[] args) throws Exception {
      // TODO Auto-generated method stub
      FastReader sc = new FastReader();
      BufferedWriter ou = new BufferedWriter(new OutputStreamWriter(System.out));
      // Start coding
      int tc = sc.nextInt();
      for (int o = 0; o < tc; o++) {
         int n = sc.nextInt();
         int a[] = new int[n];
         int f[] = new int[n];
         for (int i = 0; i < n; i++) {
            a[i] = sc.nextInt();
         }
         Arrays.fill(f, 0);
         for (int i = 0; i < n; i++) {
            for (int j = 0; j < n; j++) {
               if (a[i] == a[j]) {
                  f[i]++;
               }
            }
         }

         int max = 1;
         int k = 0;
         int count = 0;
         for (int i = 0; i < n; i++) {
            if (f[i] > max) {
               max = f[i];
               k = i;
            }
         }
         for (int i = 0; i < n; i++) {
            if (f[k] == f[i]) {
               count++;
               if (count > f[k]) {
                  ou.write("CONFUSED" + "\n");
                  break;
               }
            }
         }
         if (count == f[k]) {
            ou.write(a[k] + "\n");
         }

      }
      ou.flush();
   }
}
```
### Time Taken: 20 min

### Problem #4  [Beat the Average](https://www.codechef.com/START37D/problems/ABOVEAVG) 
#### 
#### Related Topics:

Math

#### Code:
```java
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;
import java.lang.Math;
import java.util.*;
import java.io.*;
import java.util.*;
import java.util.StringTokenizer;

import javax.lang.model.element.Element;

public class Main {
   static class FastReader {
      BufferedReader br;
      StringTokenizer st;

      public FastReader() {
         br = new BufferedReader(new InputStreamReader(System.in));
      }

      String next() {
         while (st == null || !st.hasMoreElements()) {
            try {
               st = new StringTokenizer(br.readLine());
            } catch (IOException e) {
               e.printStackTrace();
            }
         }
         return st.nextToken();
      }

      int nextInt() {
         return Integer.parseInt(next());
      }

      long nextLong() {
         return Long.parseLong(next());
      }

      double nextDouble() {
         return Double.parseDouble(next());
      }

      String nextLine() {
         String str = "";
         try {
            str = br.readLine();
         } catch (IOException e) {
            e.printStackTrace();
         }
         return str;
      }
   }

   public static void main(String[] args) throws Exception {
      // TODO Auto-generated method stub
      FastReader sc = new FastReader();
      BufferedWriter ou = new BufferedWriter(new OutputStreamWriter(System.out));
      // Start coding
      int tc = sc.nextInt();
      for (int o = 0; o < tc; o++) {
         int n = sc.nextInt();
         int m = sc.nextInt();
         int x = sc.nextInt();

         int t = n * x;

         if (m <= x) {
            ou.write(0 + "\n");
         } else {
            ou.write(t / (x + 1) + "\n");

         }
      }
      ou.flush();
   }
}
```
### Time Taken: 10 min