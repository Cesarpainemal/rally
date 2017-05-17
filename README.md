# rally
 public static void main(String[] args) {
      
        Scanner entrada = new Scanner(System.in);
    
        int competidores;
        String [] nombres ;
        
        
        System.out.println("Cantidad de competidores");
        competidores = entrada.nextInt();
        nombres = new String [competidores]; 
        
        for (int i=0;i<competidores;i++){
            System.out.print("ingrese nombre "+(i+1)+ ": ");
            nombres [i]= entrada.next();
        }
        
        System.out.println("cuanto tramos ");
        int tramos = entrada.nextInt();
        while (tramos<=0){
            System.out.println("Ingrese nuevamente los tramos");
            tramos= entrada.nextInt();
        }
        int[][]tiempos1 = new int [competidores][tramos+1];
        int[][]tiempos2 = new int [competidores][tramos+1];
        int[][]tiempos3 = new int [competidores][tramos+1];
        int[][]tiempos4 = new int [competidores][tramos+1];
        int[][]tiempos5 = new int [competidores][tramos+1];
       
        int [][] tiempo_separados= new int [competidores][tramos];
        
        int []mejor_tiempo1 = new int [competidores];
        int []mejor_tiempo2 = new int [competidores];
        int []mejor_tiempo3 = new int [competidores];
        int []mejor_tiempo4 = new int [competidores];
        int []mejor_tiempo5 = new int [competidores];
       
        
        int tiempo_tramo;
        int suma; 
        
        for (int i=0;i<competidores;i++){
            for(int j=0;j<tramos+1;j++){
                if(j==0){
                tiempos1[i][j]= 0;
                tiempo_separados[i][j]=0;
                }
                else{
                    tiempo_tramo =(int)(Math.random()*99+1);
                    tiempo_separados[i][j]= tiempo_tramo;
                    
                    suma = tiempos1[i][j-1]+tiempo_tramo;
                    tiempos1[i][j]=suma;
                }  
            }
        }
        for (int i=0;i<competidores;i++){
            suma_de_tiempos[i]= tiempos1[i][tramos];
            suma_de_tiempos[i]= suma_de_tiempos[i] tiempos2[i][tramos]
            suma_de_tiempos[i]= suma_de_tiempos[i] tiempos3[i][tramos]
            suma_de_tiempos[i]= suma_de_tiempos[i] tiempos4[i][tramos]
            suma_de_tiempos[i]= suma_de_tiempos[i] tiempos5[i][tramos]

    
    }
        
        
        for (int i=0;i<competidores;i++){
            for(int j=0;j<tramos;j++){

                System.out.print(tiempos1[i][j]+" ");

            }
            System.out.print("\n");

        }
	
    }
    
}
