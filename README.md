# Lab_7

import java.io.File;
import java.io.IOException;
import java.io.RandomAccessFile;
import java.util.Scanner;
public class Lab7 {
    public static void main(String[] args) throws IOException{
        Scanner sc = new Scanner(System.in);
        System.out.println("Количество театров? ");
        int count = sc.nextInt();
        sc.nextLine();
        RandomAccessFile rf, df;
        String name , place,address,rating, Path1 = "C:\\World\\workers.txt",Path2 = "C:\\World\\answer.txt";
        try{
            File f1 = new File(Path1);
            File f2 = new File(Path2);
            rf = new RandomAccessFile(f1, "r");
            df = new RandomAccessFile(f2, "r");

            for (int i = 0; i < count; i++) {
                System.out.println("Введите название театра ");
                name = sc.nextLine();
                rf.writeUTF(name);
                for (int j = 0; j < 20 - name.length(); j++) {
                    rf.writeByte(1);
                }
                System.out.println("Художественный руководитель ");
                place = sc.nextLine();
                rf.writeUTF(place);
                for (int j = 0; j < 20 - place.length(); j++) {
                    rf.writeByte(1);
                }
                System.out.println("Введите адрес ");
                address = sc.nextLine();
                rf.writeUTF(address);
                for (int j = 0; j < 20 - address.length(); j++) {
                    rf.writeByte(1);
                }
                System.out.println("Введите рейтинг ");
                rating = sc.nextLine();
                rf.writeUTF(rating);
                for (int j = 0; j < 20 - rating.length(); j++) {
                    rf.writeByte(1);
                }
                System.out.println();
                if (name.equals("Москва")){
                    df.writeUTF(name);
                    for (int j = 0; j < 20 - name.length(); j++) df.writeByte(1);
                    df.writeUTF(place);
                    for (int j = 0; j < 20 - place.length(); j++) df.writeByte(1);
                    df.writeUTF(address);
                    for (int j = 0; j < 20 - address.length(); j++)df.writeByte(1);
                    df.writeUTF(rating);
                    for (int j = 0; j < 20 - rating.length(); j++)df.writeByte(1);
                }
            }
        }catch (Exception e){
            e.printStackTrace();
        }
    }
}

