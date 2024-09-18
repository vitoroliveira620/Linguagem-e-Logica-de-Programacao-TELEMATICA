#include <stdio.h>
#include <stdlib.h>

// Definição da estrutura de produto
typedef struct {
    int codigo;
    char descricao[50];
    float valorUnitario;
    int qtdEstoque;
    float valorEstoque;
} Produto;

// Função para exibir o menu principal
void exibirMenu() {
    printf("----------------------------------------------------------------------\n");
    printf("Sistema de Estoque\n");
    printf("----------------------------------------------------------------------\n");
    printf("1) Entrada de Produtos\n");
    printf("2) Listar os Produtos\n");
    printf("3) Valor Total do Estoque\n");
    printf("4) Fim\n");
    printf("Opção: ");
}

// Função para cadastrar um produto
void cadastrarProduto(Produto *produto) {
    printf("----------------------------------------------------------------------\n");
    printf("Entrada de Cadastro de Produtos\n");
    printf("----------------------------------------------------------------------\n");
    printf("Código: ");
    scanf("%d", &produto->codigo);
    printf("Descrição: ");
    scanf("%s", produto->descricao);
    printf("Valor Unitário: ");
    scanf("%f", &produto->valorUnitario);
    printf("Qtd Estoque: ");
    scanf("%d", &produto->qtdEstoque);
    produto->valorEstoque = produto->valorUnitario * produto->qtdEstoque;
    printf("Valor Estoque: %.2f\n", produto->valorEstoque);
}

// Função para gravar os dados do produto em um array
void gravarDados(Produto *produto, Produto *produtos, int *tamanho) {
    produtos[*tamanho] = *produto;
    (*tamanho)++;
}

int main() {
    int opcao;
    int tamanho = 0;
    Produto produtos[100]; // Array para armazenar os produtos
    Produto produto;

    do {
        exibirMenu();
        scanf("%d", &opcao);

        switch (opcao) {
            case 1:
                cadastrarProduto(&produto);
                printf("Digite (1-Para Gravar, 2-Voltar a tela inicial) : ");
                int escolha;
                scanf("%d", &escolha);
                if (escolha == 1) {
                    gravarDados(&produto, produtos, &tamanho);
                }
                break;
            case 2:
                // Listar os produtos (ainda não implementado)
                break;
            case 3:
                // Valor Total do Estoque (ainda não implementado)
                break;
            case 4:
                printf("Fim do programa.\n");
                break;
            default:
                printf("Opção inválida. Por favor, escolha uma opção válida.\n");
        }
    } while (opcao != 4);

    return 0;
}
