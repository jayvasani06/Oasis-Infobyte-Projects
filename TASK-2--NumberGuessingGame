import java.util.*;
public class Main {
    public static void main(String[] args) {
        Random rand = new Random();
        Scanner sc = new Scanner(System.in);
        System.out.println("******WELCOME TO NUMBER GUESSING GAME******");
        System.out.println("\nIN THE GAME IT'S HAVE A ATTEMT :5");
        System.out.println("IN THE GAME IT'S HAVE A ROUND :3");
        int MaxAttempt=5;
        int MaxRound=3;
        int MaxNumber=100;
        int MinNumber=1;
        int TotalScore=0;

        for(int i=1;i<=MaxRound;i++){
            int RandomNumber = rand.nextInt(MaxNumber)+MinNumber;
            int CurrentAttempt=0;
            System.out.println("\n****** Current round "+i+" ******");
            System.out.println("Guess The Nmber Between 1 To 100 in 5 Attempt!");
            while(CurrentAttempt<MaxAttempt){
                System.out.println("\nEnter Your Guess");
                int GuessNumber=sc.nextInt();
                CurrentAttempt+=1;
                if(GuessNumber==RandomNumber){
                    int Score = MaxAttempt - CurrentAttempt;
                    TotalScore+=Score;
                    System.out.println("Congrats! Your Succesfully Guess The Number.\nAttemt :"+CurrentAttempt+
                            " Round Score :"+Score);
                    break;
                } else if (GuessNumber>RandomNumber) {
                    System.out.println("The Number Is Grater That "+GuessNumber+
                            " Attempt Left :"+(MaxAttempt - CurrentAttempt));
                } else if (GuessNumber<RandomNumber) {
                    System.out.println("The Number Is Less That "+GuessNumber+
                            " Attempt Left :"+(MaxAttx
            }
            if(CurrentAttempt==MaxAttempt){
                System.out.println("Ops! Your Lost This Round!!");
                System.out.println("Round :"+i+" Attempt :0");
                System.out.println("\nThe Random Number is :"+RandomNumber);
            }
        }
        System.out.println("Game Is Over! Your Total Score Is "+TotalScore);
    }
}
