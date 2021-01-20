# Manipulando-arays-em-JavaSE 
Nessas poucas linhas de codigos en java eu  consegui criar um programa que  da a opção de escolher de forma manual ou automática o número de linhas
e coluna que tarão a matriz, depois escolher se o preencimeto também é manual ou autom.
Nem sei se estou correto, mas é coisa de principiante.
Comecei no java há seis meses.

package pssword;
import java.util.Scanner;
public class Pssword {
    public static void main(String[] args) {
        Scanner input=new Scanner(System.in);        
int x = 0,y = 0,i,j,modo1,modo2;        
        System.out.println("Digite 1 para número de linhas e colunas aleatórios");
        System.out.println("Digite 2 para inserir número de linhas e colunas manualmente");
        modo1=input.nextInt();       
        switch (modo1) {
            case 1:
                x=(int)(Math.random()*30);
                y=(int)(Math.random()*30);
                break;
            case 2:
                System.out.println("Digite o número de linhas desejado na matriz");
                x=input.nextInt();
                System.out.println("Digite o número de colunas desejado na matriz");
                y=input.nextInt();
                break;
            default:
                System.err.println("Opção inválida");
                break;
        }       
        int [][] caixa01 = new int [x][y];
        int [][] caixa02 = new int [x][y];
        int [][] soma = new int [x][y];              
        System.out.println("Digite 1 para preecher automaticamente");
        System.out.println("Digite 2 para preencher manualmente");
        modo2=input.nextInt();        
        switch (modo2){        
            case 2:
 System.out.println("Digite os valores da matriz 1 de "+ x +" x "+ y);
        for (i=0; i<x; i++){
            for (j=0; j<y; j++){            
                System.out.println("Digite a posição "+(i+1)+"x"+(j+1)+"da matriz");
                caixa01[i][j]=input.nextInt();
            }
        }             
         System.out.println("Digite os valores da matriz 2 de "+ x +" x "+ y);
        for (i=0; i<x; i++){
            for (j=0; j<y; j++){            
                System.out.println("Digite a posição "+(i+1)+"x"+(j+1)+"da matriz");
                caixa02[i][j]=input.nextInt();
            }
        }                
                break;
            case 1 : 
                for (i=0; i<x; i++){
            for (j=0; j<y; j++){            
            caixa01[i][j]= (int)(Math.random()*51);
            }
        }        
        for (i=0; i<x; i++){
            for (j=0; j<y; j++){            
            caixa02[i][j]= (int)(Math.random()*51);
            }
        }                
                break;
            default:
                System.err.println("Opção inválida");
                break;       
        }  
        for (i=0; i<x; i++){
            for (j=0; j<y; j++){
                soma[i][j]=caixa01[i][j]+caixa02[i][j];         
            }
        }        
        for (i=0; i<x; i++){
            for (j=0; j<y; j++){
                System.out.print(soma[i][j]+"  ");                         
            }
            System.out.println("");
        }
        System.out.println("Matriz com "+x+" linhas e "+y+" colunas"); 
        }
        }
