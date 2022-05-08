# Day 5

## Number of Problems Solved: 2

### Problem #1 [Game of Pooks](https://www.codechef.com/problems/POOK)

#### Related Topics:
Chess
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
import javax.lang.model.util.ElementScanner6;

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

            if(n==2 || n==3){
                ou.write(n-1 + "\n");
            }
            else
            {
                ou.write(n + "\n");
            }
        }
        ou.flush();
    }
}
```

#### Time Taken: 5 min

### Problem #2 [ATM Machine](https://www.codechef.com/problems/ATM2)

#### Related Topics:

Implementation, Algorithms

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
import javax.lang.model.util.ElementScanner6;

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
            int k = sc.nextInt();

            int sum = 0;
            int ar[] = new int[n];
            for (int i = 0; i < n; i++) {
                ar[i] = sc.nextInt();
                if ((k-sum)>=ar[i]) {
                    ou.write(1 + "");
                    sum = sum + ar[i];
                }
                else
                {
                    ou.write(0 + "");
                }
            }
            ou.write("\n");
        }
        ou.flush();
    }
}
```

#### Time Taken: 3 mins
