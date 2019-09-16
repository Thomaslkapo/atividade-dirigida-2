# Thomas
#include <iostream>
#include <vector>
#include <algorithm>


using namespace std;
int main(){
    int resposta, opcao, i, soma = 0;
    vector <int> numeros ;
    do {
    cout <<"Digite um valor inteiro"<< endl;
    cin >> i;
    numeros.push_back(i);
    cout << "Voce quer digitar outro valor inteiro? (diigite 1 para sim e 2 para nao)"<< endl;
    cin >> resposta;
    if(resposta == 1){
    }
    }while(resposta == 1);
    cout << "Digite [1] para ver a soma dos elementos" << endl;
    cout << "Digite [2] para ver a media dos elementos" << endl;
    cout << "Digite [3] para ver a media e o somatorio dos elementos" << endl;
    cout << "Digite [4] para substituir  por zero todos os valores negativos e imprimir a media" << endl;
    cout << "Digite [5] para substituir por zero todos os valores repetiodos e imprimir a media e o somatorio" << endl;
    cout << "Digite [6] para obter os elementos da lista ordenada" << endl;
    cin >> opcao;
        switch(opcao){
    case 1:
        for( i = 0; i < numeros.size();i ++){
        soma = soma + numeros[i];

    }   cout << "Soma e igual a: " << soma << endl;
        break;
    case 2:
        for( i = 0; i < numeros.size();i ++){
        soma = soma + numeros[i];

    }   cout << "Media e igual a: " << soma/numeros.size() << endl;
        break;
    case 3:
        for( i = 0; i < numeros.size();i ++){
        soma = soma + numeros[i];
    }cout << "A Media e a Soma dos elementos e igual a: " << endl <<"Media = "<<soma/numeros.size() << endl << "Soma = " << soma << endl;
        break;
    case 4:
        for (int i = 0; i < numeros.size(); ++i) {
            if (numeros[i] < 0){
                numeros[i] = 0;
            }
            soma = soma + numeros[i];
        }cout << "Media sem numeros negativos e igual a = " << soma/numeros.size() << endl;
        break;
    case 5 :
        for (int x = 0; x < numeros.size(); x++) {
        for (int y = 0; y < numeros.size(); y++) {
        if (x != y && numeros[x] == numeros[y]){
        numeros[y] = 0;
  }
 }
} for( i = 0; i < numeros.size();i ++){
        soma = soma + numeros[i];
   }

        cout << "A Media e a Soma dos elementos sem os numeros repitidos e igual a : " << endl << "Media = " << soma / numeros.size() << endl << "Soma = " << soma << endl;
        break;
    case 6 :

        sort(numeros.begin(), numeros.end());
        cout << "[";
        for (int x  : numeros) {
        cout << x << ",";
        }cout << "]";
        break;
        }
    return 0;
}



