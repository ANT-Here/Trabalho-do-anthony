# Trabalho-do-anthony
/*
Programa: [Dice 12]
Data: 2025.12.03
Estudante: [Anthony Pagani]
Objetivo: Rolar o dado duas vezes e somar depois e fazer isso denovo ou nao.
*/

import java.util.Scanner;
import java.util.Random;

public class Main {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        Random r = new Random();

        System.out.println("Press R to start rolling the dice."); // Pra comecar a secao
        System.out.println("Press X to exit the program."); // Pra encerar a secao

        while (true) {
            String key = input.next();

            if (key.equalsIgnoreCase("R")) {
                // Vai roletar aleatoriamente os números do dado
                int Roll = r.nextInt(6);
                int Rolled;

                if (Roll == 1) {
                    Rolled = 1;
                } else if (Roll == 2) {
                    Rolled = 2;
                } else if (Roll == 3) {
                    Rolled = 3;
                } else if (Roll == 4) {
                    Rolled = 4;
                } else if (Roll == 5) {
                    Rolled = 5;
                } else {
                    Rolled = 6;
                }

                // Vai guardar duas rolagens do dado
                int A = r.nextInt(Rolled) + 1;
                int B = r.nextInt(Rolled) + 1;

                // Somará as rolagens do dado
                double M = A + B;

                // Resultado após rolar o dado duas vezes
                System.out.println("Roll 1 = " + A);
                System.out.println("Roll 2 = " + B);
                System.out.println(String.format("You Rolled = %.0f", M));
                System.out.println("Press R to roll again or X to leave");
            } 
            else if (key.equalsIgnoreCase("X")) {
                break; // Botao pra sair do jogo
            }
        }
    }
}
