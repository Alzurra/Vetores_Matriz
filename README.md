# Vetores_Matriz
C++

#include <iostream>
#include <time.h>

using namespace std;

int main()
{
    int v[5];
    int menor;
    int maior;
    int somav=0;
    int somab=0;
    int somatotal=0;
    
    int b[5];
    int c[5];
    
    srand(time(NULL));
    for(int i=0;i<5;i++){
        //cout<<"Digite um número POSIÇÃO ["<<i<<"]: ";
        v[i]=rand()%11;
        cout<<"["<<v[i]<<"]"<<" ";
        
    }
    cout<<endl;
    cout<<endl;
    for(int i=0;i<5;i++){
        if(i==0){
            maior = menor = v[i];
        }else if(v[i]>maior){
            maior = v[i];
        }else if(v[i]<menor){
            menor = v[i];
        }
    }
    
    for(int i=0;i<5;i++){
        v[i]=rand()%10;
        somav+=v[i];
        cout<<"VETOR V[I]----->["<<v[i]<<"]"<<" ";
    }
    cout<<endl;
    cout<<endl;
    for(int i=0;i<5;i++){
        b[i]=rand()%10;
        somab+=b[i];
        cout<<"VETOR B[I]----->["<<b[i]<<"]"<<" ";
    }
    cout<<endl;
    cout<<endl;
    for(int i=0;i<5;i++){
        somatotal=somav+somab;
        c[i]=v[i]+b[i];
        cout<<"Soma dos valores entre o vetor v[i] Position["<<i<<"]"<<" e o vetor b[i] Position["<<i<<"] = "<<c[i]<<endl;
        cout<<"A soma total dos dois vetores é = "<<somatotal<<endl;
        
    }
    
    
    cout<<endl;
    cout<<"Maior = "<<maior<<endl;
    cout<<"Menor = "<<menor<<endl;
    
    int mat[4][4];
    int cont=0;
    int soma=0;
    int ma;
    int me;
    
    srand(time(NULL));
    for(int l=0;l<4;l++){
        for(int c=0;c<4;c++){
            mat[l][c]=rand()%100;
            cont++;
            soma+=mat[l][c];
            if(l==0 && c==0){
                ma = me = mat[l][c];
            }else if(mat[l][c]>ma){
                ma = mat[l][c];
            }else if(mat[l][c]<me){
                me = mat[l][c];
            }
        }
    }
    
    cout<<"O maior valor dentro da matriz é o número: "<<ma<<endl;
        cout<<"O menor valor dentro da matruz é o número: "<<me<<endl;
    for(int l=0;l<4;l++){
        for(int c=0;c<4;c++){
           cout<<"["<<mat[l][c]<<"]";
        }
        cout<<endl;
    }
    cout<<endl;
    cout<<"Total de elementos dentro do array = "<<cont<<endl;
    cout<<"O total da soma dos elementos dentro da matriz é = "<<soma<<endl;
    
    return 0;
}
