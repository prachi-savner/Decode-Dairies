import java.util.Scanner;

public class DecodeDairies{

       public static void main(String args[]){
              Scanner sc=new Scanner(System.in);
              System.out.print("Enter number of days : ");
              int N=sc.nextInt();

              int sunbuds=0,moonblossoms=0,starroots=0,crystalFlower=0,wildleaf=0,restingDays=0;

              for(int i=1;i<=N;i++){
                     if(i%2==0||i%3==0||i%4==0){
                            if(i%2==0&&i%3==0&&i%4==0){
                                   restingDays+=1;
                            }
                            if(i%2==0&&i%3==0){
                                   crystalFlower+=1;
                            }
                            if(i%2==0){
                                   sunbuds+=2;
                            }
                            if(i%3==0){
                                   moonblossoms+=3;
                            }
                            if(i%4==0){
                                   starroots+=4;
                            } 
                     }
                     else{
                            wildleaf+=1;
                     }
              }
              int totalFlowers=sunbuds+moonblossoms+starroots+wildleaf+crystalFlower;

              System.out.println("Sunbuds = "+sunbuds);
              System.out.println("Moonblossoms = "+moonblossoms);
              System.out.println("CrystalFlowers = "+crystalFlower);
              System.out.println("Starroots = "+starroots);
              System.out.println("Wildleaf = "+wildleaf);
              System.out.println("Resting Days = "+restingDays);
              System.out.println("Total flowers = "+totalFlowers);


       }
}
