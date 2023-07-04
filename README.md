# ARRAYS2D
//Transpose Matrix
//SOURCE CODE
import java.io.*;
import java.util.*;
public class Solution {
    public static void main(String[] args) {
        Scanner sc=new Scanner(System.in);
        int n=sc.nextInt();
        int ar[][]=new int[n][n];
        for(int i=0;i<n;i++)
        {
            for(int j=0;j<n;j++){
                ar[i][j]=sc.nextInt();
            }
        }
        for(int i=0;i<n;i++){
            for(int j=0;j<n;j++){
                System.out.print(ar[i][j]+" ");
            }
            System.out.println();
        }
        System.out.println("Transpose matrix is:");
        for(int i=0;i<n;i++)
        {
            for(int j=0;j<n;j++)
            {
                System.out.print(ar[j][i]+" ");
            }
            System.out.println();
        }
        
    }
}

//Matrix Multiplication
//SOURCE CODE
import java.io.*;
import java.util.*;
public class Solution {
    public static void main(String[] args) {
        Scanner sc=new Scanner(System.in);
        int m=sc.nextInt();
        int f=sc.nextInt();
        int ar[][]=new int[m][f];
        for(int i=0;i<m;i++)
        {
            for(int j=0;j<f;j++)
            {
                ar[i][j]=sc.nextInt();
            }
        }
        int ar1[][]=new int[m][f];
        for(int i=0;i<m;i++)
        {
            for(int j=0;j<f;j++)
            {
                ar1[i][j]=sc.nextInt();
            }
        }
        int ar2[][]=new int[m][f];
        for(int i=0;i<m;i++)
        {
            for(int j=0;j<f;j++)
            {
                ar2[i][j]=0;
                for(int k=0;k<m;k++){
                    ar2[i][j]+=ar[i][k]*ar1[k][j];
                }
                System.out.print(ar2[i][j]+" ");
            }
            System.out.println();
        }        
    }
}

//Sum of Zig-Zag
//SOURCE CODE
import java.io.*;
import java.util.*;
public class Solution {
    public static void main(String[] args) {
        Scanner sc=new Scanner(System.in);
        int m=sc.nextInt();
        int f=sc.nextInt();
        int ar[][]=new int[m][f];
        for(int i=0;i<m;i++)
        {
            for(int j=0;j<f;j++)
            {
                ar[i][j]=sc.nextInt();
            }
        }
        int sum=0;
        int temp=f;
        for(int i=0;i<m;i++)
        {
            if (i==0||i==m-1)
            {
                for(int j=0;j<f;j++)
                {
                    sum+=ar[i][j];
                }
            }
            else {
                for(int j=0;j<f;j++)
                {
                    if((i+j)==(m-1))
                    {
                        sum+=ar[i][j];
                    }
                }
            }
        }
        System.out.print("Sum of Zig-Zag pattern is "+sum);
    }
}
