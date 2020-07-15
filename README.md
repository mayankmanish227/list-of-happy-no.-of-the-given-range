# list-of-happy-no.-of-the-given-range



import java.util.*;
import java.io.*;

public class HelloWorld
{

     public static void main(String []args)
     {
         Scanner sc=new Scanner(System.in);
         int l=sc.nextInt();
         int h=sc.nextInt();
        List<Integer> li=happy(l,h);
        for(int  i=0;i<li.size();i++)
        {
            System.out.println(li.get(i));   
        }
         
     }
      static List<Integer> happy(int l,int h)
     {
        List<Integer> li1=new ArrayList<>();
        for(int i=l;i<=h;i++)
       {
           int temp=i;
           int sum=0;
           int rem=0;
           while(sum!=1 && sum!=4)
           {
               sum=0;
               while(temp!=0)
               {
                   rem=temp%10;
                   sum=sum+rem*rem;
                   temp=temp/10;
                   
               }
               temp=sum;
           }
           if(sum==1 )
           {
               li1.add(i);
           }
       }
         
       return li1;  
     }
}
