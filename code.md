package com.javarush.test.level04.lesson04.task10;

/* Три числа
Ввести с клавиатуры три целых числа. Определить, имеется ли среди них хотя бы одна пара равных между собой чисел.
Если такая пара существует, вывести на экран числа через пробел. Если все три числа равны между собой, то вывести все три.
Пример для чисел 1 2 2:
2 2
Пример для чисел 2 2 2:
2 2 2
*/

import java.io.*;

public class Solution {

    public static void main(String[] args) throws Exception {
        BufferedReader reader = new BufferedReader(new InputStreamReader(System.in));

        String sNumber1 = reader.readLine();
        int a = Integer.parseInt(sNumber1);
        String sNumber2 = reader.readLine();
        int b = Integer.parseInt(sNumber2);
        String sNumber3 = reader.readLine();
        int c = Integer.parseInt(sNumber3);
        int d = 4;

        if (a == b) {
            d = 1;
            if (b == c)
                d = 3;
        }
        if (d != 3)
            if (b == c)
                d = 2;

        switch (d) {
            case 1:
                System.out.println(a + " " + b);
                break;
            case 2:
                System.out.println(b + " " + c);
                break;
            case 3:
                System.out.println(a + " " + b + " " + c);
                break;
            case 4:
                System.out.println("Одинаковых чисел нет.");
        }
    }
}
