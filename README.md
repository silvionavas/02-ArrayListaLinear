# Roteiro da Atividade Prática – Lista Linear em C++

## Objetivo da Atividade
O objetivo desta atividade é **compreender e praticar a manipulação de listas lineares** utilizando **arrays em C++**.  
Ao final, você deverá implementar a função `buscarElemento()`, que será responsável por procurar um número digitado pelo usuário dentro da lista.

---

## Revisão Conceitual – Arrays em C++

Antes de iniciar a implementação, é importante relembrar o conceito de **array** em C++:

- Um **array** é uma estrutura de dados que armazena **um conjunto de elementos do mesmo tipo**, em posições de memória contíguas.  
- Cada elemento pode ser acessado por meio de um **índice** (posição), que inicia em **0**.
- Em C++ os arrays possuem **tamanho fixo**, definido em sua declaração.

### Exemplo de declaração e uso:
```cpp
int numeros[5]; // array de inteiros com 5 posições (índices 0 a 4)

numeros[0] = 10; // atribui valor 10 ao primeiro elemento
numeros[1] = 20; // atribui valor 20 ao segundo elemento

cout << numeros[0]; // exibe: 10
cout << numeros[1]; // exibe: 20
```

### Características importantes:
1. O acesso a elementos é **rápido (O(1))**, pois é feito diretamente pelo índice.
2. O tamanho do array é **estático**, definido no momento da compilação.
3. Arrays podem ser utilizados como base para estruturas mais complexas, como listas lineares, filas e pilhas.

No código fornecido, o array `lista[MAX]` é usado como base para armazenar os elementos da lista linear.

---

## Estrutura do Programa Base

O programa já contém algumas funções implementadas:
- **`inicializar()`** → limpa a lista, definindo que não há elementos.
- **`exibirQuantidadeElementos()`** → mostra quantos elementos estão armazenados.
- **`exibirElementos()`** → lista todos os elementos já inseridos.
- **`inserirElemento()`** → adiciona um novo valor à lista, se houver espaço.
- **`menu()`** → apresenta opções para o usuário interagir com o programa.

A função **`buscarElemento()`** foi deixada em aberto e será a sua tarefa implementar.

---

## Tarefa – Implementar `buscarElemento()`

### Requisitos da função:
1. Pedir para o usuário digitar um número.
2. Percorrer o array `lista` e procurar esse número.
3. Caso o número seja encontrado:
   - Exibir a **posição (índice)** em que ele se encontra.
4. Caso não seja encontrado:
   - Exibir a mensagem `"Elemento não encontrado"`.

### Dicas de implementação:
- Utilize um **laço `for`** para percorrer os elementos do array até `nElementos`.
- Use uma variável auxiliar (por exemplo, `bool encontrado`) para controlar se o número foi achado ou não.
- Lembre-se que o índice no array começa em `0`, mas você pode exibir a posição ao usuário de forma mais “natural” (exemplo: posição 1 para o primeiro elemento).

---

## Exemplo esperado de interação

```
Menu Lista Linear

1 - Inicializar Lista
2 - Exibir quantidade de elementos
3 - Exibir elementos
4 - Buscar elemento
5 - Inserir elemento
6 - Sair

Opcao: 5
Digite o elemento: 25

Opcao: 5
Digite o elemento: 40

Opcao: 4
Digite o elemento a buscar: 40
Elemento encontrado na posição 2

Opcao: 4
Digite o elemento a buscar: 99
Elemento não encontrado
```

---

## Desafio Extra (opcional)

- Modifique a função `buscarElemento()` para que, caso o elemento ocorra **mais de uma vez na lista**, todas as posições sejam exibidas.
- Exemplo:
  ```
  Lista = [10, 20, 30, 20, 40]
  Busca por 20
  Resultado: encontrado nas posições 2 e 4
  ```
