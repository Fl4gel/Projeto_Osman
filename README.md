# Projeto_Osman
Entrega do projeto
Depósito do projeto para o professor Osman
Entrega dia 30/06
Base já pronta 


Alterações funcionando da opção "0" e "1": - CAIO

PELO PEDRO

// Correções realizadas no código:

1. Renomeação da estrutura 'Marca' para 'Fabricante':
   - A estrutura 'Marca' foi renomeada para 'Fabricante' em todo o código, garantindo consistência.

2. Atualização das referências à estrutura 'Fabricante':
   - Todas as referências à estrutura 'Marca' foram atualizadas para 'Fabricante' em todo o código.
   - Isso inclui as entradas e saídas de dados, como a exibição da lista de marcas/fabricantes.

3. Remoção de trechos de código desnecessários:
   - Foram removidos trechos de código que tratavam a marca e o fabricante como entidades separadas, já que agora utilizamos apenas a estrutura 'Fabricante'.

4. Atualização dos menus e exibições de dados:
   - Os menus foram atualizados para refletir a mudança de 'Marca' para 'Fabricante'.
   - As exibições de dados foram atualizadas para utilizar a informação correta do fabricante associado ao produto.

5. Ajustes nos loops e ordenação dos produtos:
   - Os loops de ordenação dos produtos foram corrigidos para utilizar a estrutura correta e garantir a ordenação adequada.
   - Agora os produtos são ordenados com base no 'valor do lucro' e 'percentual de lucro' corretamente.

6. Correção nas mensagens de saída:
   - As mensagens de saída foram ajustadas para refletir corretamente as informações sobre fabricantes e marcas.

7. Remoção do limite máximo de marcas e produtos:
   - O código foi modificado para remover o limite máximo de marcas (anteriormente definido como MAX_MARCAS) e produtos (anteriormente definido como MAX_PRODUTOS).
   - Agora, o tamanho dos arrays `marcas` e `produtos` é dinamicamente redimensionado à medida que novas marcas e produtos são cadastrados, utilizando as funções `malloc` e `realloc`.
   - Isso permite cadastrar quantas marcas e produtos forem necessários, sem restrições pré-definidas.

8. Uso das funções `malloc` e `realloc` para alocação dinâmica de memória:
   - Foram utilizadas as funções `malloc` e `realloc` para alocar e realocar memória dinamicamente para os arrays `marcas` e `produtos`.
   - Isso permite que o código se adapte ao número de marcas e produtos cadastrados, garantindo flexibilidade no armazenamento dos dados.

9. Liberação de memória alocada dinamicamente:
   - Ao final do programa, foi adicionado o código para liberar a memória alocada dinamicamente utilizando a função `free`.
   - Isso garante a correta liberação dos recursos utilizados pelo programa, evitando vazamentos de memória.


