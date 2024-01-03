# Rock-paper-scissors game without methods
import java.util.Random;
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner k = new Scanner(System.in);
        Random rnd = new Random();

        System.out.println("Taş-Kağıt-Makas Oyunu");
        System.out.println("1. Taş");
        System.out.println("2. Kağıt");
        System.out.println("3. Makas");
        System.out.print("Seçiminizi yapın (1-3): ");

        int kullaniciSecimi = k.nextInt();

        if (kullaniciSecimi >= 1 && kullaniciSecimi <= 3) {
            String[] secenekler = {"Taş", "Kağıt", "Makas"};
            int bilgisayarSecimi = rnd.nextInt(3) + 1;

            System.out.println("Bilgisayarın Seçimi: " + secenekler[bilgisayarSecimi - 1]);
            System.out.println("Kullanıcının Seçimi: " + secenekler[kullaniciSecimi - 1]);

            if (bilgisayarSecimi == kullaniciSecimi) {
                System.out.println("Berabere");
            } else if (bilgisayarSecimi == 1 && kullaniciSecimi == 3) {
                System.out.println("pc kazandı");
            } else if (bilgisayarSecimi == 1 && kullaniciSecimi == 2){
                System.out.println("oyuncu kazandı");}
            else if (bilgisayarSecimi==2 && kullaniciSecimi==1){
                System.out.println("pc kazandı");}
            else if (bilgisayarSecimi==3&&kullaniciSecimi==1){
                System.out.println("oyuncu kazandı");}
            else if (bilgisayarSecimi==2&&kullaniciSecimi==3){
                System.out.println("oyuncu kazandı");}
            else if (bilgisayarSecimi==3&&kullaniciSecimi==2){
                System.out.println("pc kazandı");}


        }  else System.out.println("geçersiz sayı");
    }
}

