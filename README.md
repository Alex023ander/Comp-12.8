# Comp-12.8

public static void main(String[] args) {
        final int N=9;
        
        int[][] array=new int[N][N];
        
        for (int i=0;i<N;i++){
            for(int j=0;j<=i;j++){
                if(j==0||j==i){
                    array[i][j]=1;
                }
                else{
                    array[i][j]=array[i-1][j]+array[i-1][j-1];
                }
                
            }
        }
        
        for (int i = 0; i < N; i++) {
            for (int j = 0; j < N - i; j++)
                System.out.print(" ");
            for (int k = 0; k <=i; k++)
                System.out.print(array[i][k]+" ");
            System.out.println();
        }
    }
    
}
