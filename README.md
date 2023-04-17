# Prova técnica

**Premissa**
> Nosso novo cliente possui cinco lojas de artigos diversos e precisa de um software que permita ele cadastrar os produtos do seu estoque.
> Os produtos podem ser cadastrados através de uma interface ou API. Hoje ele controla via planilha o estoque. Cada novo cadastro de produto, deverá enviar um email para o gestor da empresa, porém, em caso de alteração deverá postar via json para uma determinada api.

### Especificação
#### Produtos
| Campo | Tipo |
| ----- | ---- |
| Nome  | string |
| Quantidade | int |
| Valor | decimal/float |


### Regras de negócio
- O software deverá permitir configurar o email do gestor
- Todo o produto cadastrado deverá ser enviado para o gestor
- Todo produto cadastrado com menos de 5 unidades no estoque deverá eviar um segundo email ao gestor informando da baixa quantidade
- Não poderá ser cadastrado um produto com estoque negativo
- Todo produto com preço R$1,99 e estoque abaixo de 5 unidades não deverá enviar o segundo email
- Todos os campos do produto deverão ser postados para uma api

### Funcionalidades esperadas
- Tela/campo/api para configurar o email do gestor
- Uma listagem dos produtos cadastrados
- Formulário/Api para cadastro/alteração de produtos
- Tela/API para remoção dos produtos
- Postar os dados do produto para api httpbin.com quando eles forem alterados

## Teste de mesa
> Dada a aplicação desenvolvida, deve ser possível realizar o cadastro dos produtos, como por exemplo as integrações abaixo:
- Ao cadastrar um novo produto, o gestor deverá receber um email com todos os dados do produto
- Ao cadastrar um novo produto com preço R$1,99 e acima de 5 unidades, o gestor deverá receber somente um email
- Ao alterar o estoque de um produto para 4 unidades e preço R$1,99, os dados deverão ser postados para a api https://httpbin.org/post

### Avaliação
> De princípio, não estamos havaliando conhecimento em cima de uma framework/tecnologia, mas sim, em cima da solução apresentada, ou seja, o mais importante é a modelagem de domínio

- De maneira textual, responda as questões abaixo
1. Descreva/Desenhe a arquitetura utilizada na solução.
2. Descreve como a modelagem de domínio foi implementada de uma maneira que deixa a aplicação flexível.
3. Como você resolveu/resolveria problemas de resiliência na aplicação?
4. Como você resolveu/resolveria problemas de escalabilidade na aplicação?
5. Como você resolveu/resolveria problemas de rastreabilidade na aplicação?
6. Como você garantiu a qualidade da sua aplicação?

### Dicas
- Espera-se que seja escrito em C#
- Lembre-se de alguns conceitos de design/arquitetura
  - DDD
  - Hexagonal
  - Onion
  - Clean
  - CQRS
- Alguns serviços similares que permitem integrações de forma flexível
  - [IFTTT](https://ifttt.com/)
  - [Zapier](https://zapier.com/)
  - [Flow](https://flow.microsoft.com/)
  - [BeeHive](https://github.com/muesli/beehive)

### Entrega
- O prazo de entrega é de 7 dias após o fork
- As alterações realizadas após este prazo não serão avaliadas
- Commit o seu projeto neste mesmo projeto github
- Crie um arquivo **Respostas.md** com as respostas das questões e os passos para compilar/executar a aplicação
- Qualquer dúvida, entre em contato pelo email: [xama@xamasistemas.com.br](mailto:xama@xamasistemas.com.br)
