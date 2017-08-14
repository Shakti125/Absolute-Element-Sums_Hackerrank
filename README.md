# Absolute-Element-Sums_Hackerrank
import java.io.*;
import java.util.*;

public class Solution {

    public static void main(String[] args) {
        /* Enter your code here. Read input from STDIN. Print output to STDOUT. Your class should be named Solution. */
        Scanner scan=new Scanner(System.in);
        int N,Q;
        N=scan.nextInt();
        int[] arr=new int[N];
        for(int i=0;i<N;i++){
            arr[i]=scan.nextInt();
        }
        Q=scan.nextInt();
        int[] qrr=new int[Q];
        for(int i=0;i<Q;i++){
            qrr[i]=scan.nextInt();
        }
        int[] sum=new int[Q];
        for(int i=0;i<Q;i++){
                for(int j=0;j<N;j++){
                arr[j]=arr[j]+qrr[i];
                sum[i]+=Math.abs(arr[j]);   
                }   
            System.out.println(sum[i]);
        }
        scan.close();
    }
}
