
package lab1;
import java.util.*;

public class Lab1 {
    static Scanner reader = new Scanner(System.in);
    public static void main(String[] args) {
        System.out.println("Введите количество элементов");
        int numberOfElements=reader.nextInt();
    if (numberOfElements==10 || numberOfElements==100 || numberOfElements==1000 || numberOfElements==10000)
    {
        int[] ArrayNoSort = new int[numberOfElements];
        int[] ArrayForSelection = new int[numberOfElements];
        int[] ArrayForBubble = new int[numberOfElements];
        for (int i=0;i<numberOfElements;i++){
        ArrayNoSort[i] = (int)(Math.random() * numberOfElements);
        ArrayForSelection[i]=ArrayNoSort[i];
        ArrayForBubble[i]=ArrayNoSort[i];
        }
        selectionSort(ArrayForSelection);
        bubbleSort(ArrayForBubble);
        outputArrays(ArrayNoSort, ArrayForBubble, ArrayForSelection);
    }
    }

 private static void outputArrays(int[] Array, int[] ArrayForBubble, int [] ArrayForSelection){
          System.out.println("Не сортированый массив");
     for (int i: Array){
         System.out.print(" " +i);
     }
          System.out.println();
              System.out.println("Массив сортированый пузырьком");
     for (int i: ArrayForBubble){
         System.out.print(" " +i);
     }
     System.out.println();
     System.out.println("Массив быстрой сортировки");
     for (int i: ArrayForSelection){
         System.out.print(" " +i);
     }
     System.out.println();
     
 }
    private static void bubbleSort(int[] ArrayForBubble){
        long start = System.nanoTime();

    for(int i = ArrayForBubble.length-1 ; i > 0 ; i--){
        for(int j = 0 ; j < i ; j++){
            if( ArrayForBubble[j] > ArrayForBubble[j+1] ){
                int tmp = ArrayForBubble[j];
                ArrayForBubble[j] = ArrayForBubble[j+1];
                ArrayForBubble[j+1] = tmp;
            }
        }
    }
    long end = System.nanoTime();
long traceTime = end-start;
System.out.println("Время сортировки пузырьком (наносекунды)" +traceTime);
}
    private static void selectionSort(int[] ArrayForSelection){
        long start = System.nanoTime();
       for (int i = 0; i < ArrayForSelection.length; i++) {
        int min = ArrayForSelection[i];
        int min_i = i; 
        for (int j = i+1; j < ArrayForSelection.length; j++) {
            if (ArrayForSelection[j] < min) {
                min = ArrayForSelection[j];
                min_i = j;
            }
        }
        if (i != min_i) {
            int tmp = ArrayForSelection[i];
            ArrayForSelection[i] = ArrayForSelection[min_i];
            ArrayForSelection[min_i] = tmp;
        }
     }
           long end = System.nanoTime();
long traceTime = end-start;
System.out.println("Время быстрой сортировки(наносекунды)" +traceTime);
    }   
}
