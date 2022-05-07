# Day 4
## Number of Problems Solved: 1

### Problem #1 [Chef and Gym](https://www.codechef.com/problems/CGYM) 

#### Related Topics:

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
        long tc = sc.nextInt();
        for (int o = 0; o < tc; o++) {
            int x = sc.nextInt();
            int y = sc.nextInt();
            int z = sc.nextInt();

            if (z>=(x+y)) {
                ou.write(2 + "\n");
            } else if(z>=x) {
                ou.write(1 + "\n");
            }
            else 
            {
               ou.write(0 + "\n" );
            }
        }
        ou.flush();
    }
}
```
#### Time Taken: 1 min

