void burbuja(int x[], int n){
    int i, j, aux;
    for(i=1; i<n; i++)
        for(j=0; j<n-i; j++)
            if(x[j]>x[j+1]){
                aux=x[j];
                x[j]=x[j+1];
                x[j+1]=aux;
            }
}

void seleccion(int arreglo[],int tamano){
     int i, j;
     int posMin, temp;
     for(i=0; i<tamano-1; i++){
          posMin=i;
          for(j=i+1; j<tamano; j++)
               if(arreglo[j]<arreglo[posMin])
                  posMin=j;
     temp=arreglo[i];
     arreglo[i]=arreglo[posMin];
     arreglo[posMin]=temp;
     }
}

void insercion(int a[], int tamano){
    int i,j,temporal;
    for(i=1; i<tamano; i++){
        j=i-1;
        while(j>=0 && a[j]>a[j+1]){
            temporal=a[j+1];
            a[j+1]=a[j];
            a[j]=temporal;
            j--;
        }
    }
}

int divide(int a[],int ini,int fin){
    int left,right,pivote,temp;
    pivote=a[ini];
    left=ini;
    right=fin;
    //Mientras no se cruxen los indices.
    while(left<right){
        while(a[right]>pivote)
            right--;

        while((left<right) && (a[left]<=pivote))
            left++;
        //si aun no se cruzan los indices seguimos intercambiando.
        if(left<right){
            temp=a[left];
            a[left]=a[right];
            a[right]=temp;
        }
    }

    temp=a[right];
    a[right]=a[ini];
    a[ini]=temp;
    //Nueva posicion del Pivote
    return right;
}

void quicksort(int a[],int ini,int fin){
    int pivote;
    if(ini<fin){
        pivote=divide(a,ini,fin);
        quicksort(a,ini,pivote-1);
        quicksort(a,pivote+1,fin);
    }
}

void shell(int L[],int n){
    int salto=n/2,i,j,k,aux;
    while(salto>0){
        for(i=salto; i<n; i++){
            j=i-salto;
            while(j>=0){
                k=j+salto;
                if(L[j]<=L[k])
                    j=0;
                else{
                    aux=L[j];
                    L[j]=L[k];
                    L[k]=aux;
                }
                j=j-salto;
            }
        }
        salto=salto/2;
    }
}
