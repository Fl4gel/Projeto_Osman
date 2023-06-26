# Projeto_Osman
Entrega do projeto
Depósito do projeto para o professor Osman
Entrega dia 30/06
Base já pronta 


Alterações funcionando da opção "0" e "1":

 case 0:
            {
                do
                {
                    printf("\tFabricante:\n");
                    fgets(fabricantes[i].fabricante, 100, stdin);

                    printf("\nInforme o nome da marca: ");
                    fgets(fabricantes[i].nomeM, 100, stdin);

                    printf("\nInforme o telefone: ");
                    fgets(fabricantes[i].telefone, 100, stdin);

                    printf("\nInforme o site: ");
                    fgets(fabricantes[i].site, 100, stdin);

                    printf("Unidades da Federacao cadastradas:\n");
                    for (j = 0; j < MAX_UF; j++)
                    {
                        printf("%d. %s\n", j + 1, unidadesFederacao[j]);
                    }
                    int uf = -1;
                    printf("Informe o numero correspondente a sua UF: ");
                    scanf("%d", &uf);
                    getchar();

                    if (uf >= 1 && uf <= MAX_UF)
                    {
                        const char *ufEscolhida = unidadesFederacao[uf - 1];
                        memcpy(fabricantes[i].uf, ufEscolhida, strlen(ufEscolhida));
                    }
                    else
                    {
                        printf("Opcao invalida.\n");
                    }

                    printf("\n");

                    printf("Deseja cadastrar mais um fabricante? (S/N): ");
                    scanf(" %c", &b);
                    getchar();

                    i++; // Incrementa o índice do fabricante

                } while (b != 'N' && b != 'n');

                break;
            }

        case 1:
            do
            {
                printf("\tProduto:\n");

                printf("Informe a descricao do produto: ");
                scanf(" %[^\n]s", produtos[numProdutos].descricao);
                while (getchar() != '\n')
                    ;

                printf("Informe o peso do produto: ");
                scanf("%f", &produtos[numProdutos].peso);
                while (getchar() != '\n')
                    ;

                printf("Informe o valor de compra: ");
                scanf("%f", &produtos[numProdutos].valorc);
                while (getchar() != '\n')
                    ;

                printf("Informe o valor de venda: ");
                scanf("%f", &produtos[numProdutos].valorv);
                while (getchar() != '\n')
                    ;

                printf("Fabricante: ");
                int fabricanteIndice;
                while (true)
                {
                    scanf("%d", &fabricanteIndice);
                    while (getchar() != '\n')
                        ;

                    if (fabricanteIndice >= 0 && fabricanteIndice < MAX_FABRICANTES)
                    {
                        produtos[numProdutos].fabricante = fabricantes[fabricanteIndice];
                        break;
                    }
                    else
                    {
                        printf("Indice de fabricante invalido. Escreva o indice entre 0 e 1.\n");
                    }
                }

                if (produtos[numProdutos].valorc != 0)
                {
                    produtos[numProdutos].percentualLucro = (produtos[numProdutos].valorlc / produtos[numProdutos].valorc) * 100;
                }
                else
                {
                    produtos[numProdutos].percentualLucro = 0;
                }

                produtos[numProdutos].valorlc = produtos[numProdutos].valorv - produtos[numProdutos].valorc;

                produtos[numProdutos].percentualLucro = (produtos[numProdutos].valorlc / produtos[numProdutos].valorc) * 100;

                printf("\n");
                numProdutos++; // Incrementa o número de produtos

                printf("Deseja cadastrar mais um produto? (S/N): ");
                scanf(" %c", &b);
                while (getchar() != '\n')
                    ;

            } while (b != 'N' && b != 'n');
            break;
