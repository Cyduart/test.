# QUESTÃO 1
O RESULTADO SERÁ 91 


# QUESTÃO 2
import java.util.ArrayList;
import java.util.Scanner;

public class Fibonacci {
    public static ArrayList<Integer> fibonacciSequence(int n) {
        ArrayList<Integer> fibSequence = new ArrayList<>();
        fibSequence.add(0);
        fibSequence.add(1);

        while (fibSequence.get(fibSequence.size() - 1) < n) {
            int nextFib = fibSequence.get(fibSequence.size() - 1) + fibSequence.get(fibSequence.size() - 2);
            fibSequence.add(nextFib);
        }

        return fibSequence;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Digite um número para verificar se pertence à sequência de Fibonacci: ");
        int number = scanner.nextInt();
        ArrayList<Integer> sequence = fibonacciSequence(number);

        if (sequence.contains(number)) {
            System.out.println("O número " + number + " pertence à sequência de Fibonacci.");
        } else {
            System.out.println("O número " + number + " não pertence à sequência de Fibonacci.");
        }

        scanner.close();
    }
}


# QUESTÃO 3
a) 1, 3, 5, 7, 9
b) 2, 4, 8, 16, 32, 64, 128
c) 0, 1, 4, 9, 16, 25, 36, 49
d) 4, 16, 36, 64, 64
e) 1, 1, 2, 3, 5, 8, 13
f) 2, 10, 12, 16, 17, 18, 19, 20

# QUESTÃO 4
Se a lâmpada estiver acesa, o segundo interruptor controla aquela lâmpada, pois foi o último interruptor ligado antes de você entrar.
Se a lâmpada estiver apagada e a lâmpada estiver quente, então o primeiro interruptor controla aquela lâmpada.
Se a lâmpada estiver apagada e a lâmpada estiver fria, então o terceiro interruptor controla aquela lâmpada.

#QUESTÃO 5 

import java.util.Scanner;

public class InvertString {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        System.out.print("Digite uma string para inverter: ");
        String inputString = scanner.nextLine();
        
        String invertedString = "";

        for (int i = inputString.length() - 1; i >= 0; i--) {
            invertedString += inputString.charAt(i);
        }
        
        System.out.println("String invertida: " + invertedString);
        
        scanner.close();
    }
}
