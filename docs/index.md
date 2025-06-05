<h2><a href= "https://www.mackenzie.br">Universidade Presbiteriana Mackenzie</a></h2>
<h3><a href= "https://www.mackenzie.br/graduacao/sao-paulo-higienopolis/sistemas-de-informacao">Sistemas de Informação</a></h3>


<font size="+12"><center>
*&lt;MEW&gt;*
</center></font>

**Conteúdo**

- [Autores](#nome-alunos)
- [Descrição do Projeto](#introdução-do-projeto)
- [Análise de Requisitos Funcionais e Não-Fucionais](#descrição-dos-requisitos)
- [Diagrama de Atividades](#diagrama-de-atividades) 
- [Diagrama de Casos de Uso](#diagrama-de-comportamento-atores)
- [Descrição dos Casos de Uso](#descrição-das-funcões)
- [Diagrama de Senquencia](#diagrama-de-ordem-interações)
- [Diagrama de Classes](#diagrama-orientado-objetos)
- [Diagrama de Estados](#diagrama-estrutura-componente)
- [Diagrama de Implantação](#diagrama-de-hardware-software)
- [Referências](#referências)


# Autores

Ana Beatriz - 10444937

Gustavo Pan - 10426600

Pedro Caruso - 10425184

Sabrina Miyasaki - 10723723


# Descrição do Projeto
O projeto tem como objetivo criar um sistema informatizado para a Farmácia, com foco na automação dos processos de vendas, controle de estoque e cadastro de clientes. A iniciativa visa substituir o atual processo manual, minimizando erros e facilitando a gestão administrativa e financeira.

O sistema permitirá o cadastro e gerenciamento de medicamentos, clientes e vendas, realizando atualizações automáticas no estoque e fornecendo relatórios gerenciais para apoiar a tomada de decisões. Haverá também um sistema de controle de acesso, diferenciando as permissões entre atendentes e administradores.

O desenvolvimento seguirá as boas práticas da modelagem UML, abrangendo a análise de requisitos e a elaboração de diagramas estruturais, promovendo maior eficiência, precisão e agilidade nas operações cotidianas da farmácia.

*&lt;Introdução do projeto&gt;*

# Análise de Requisitos Funcionais e Não-Funcionais
Requisitos Funcionais
 

RF-01 (Cadastro).	O sistema deve permitir o cadastro de medicamentos e produtos, com nome, descrição, fabricante, lote, data de validade, quantidade em estoque e preço de venda. 

RF-02 (Cadastro).	O sistema deve permitir o cadastro de clientes com nome, CPF, telefone e histórico de compras. 

RF-03.(Estoque).	O sistema deve permitir a pesquisa de produtos disponíveis no estoque. 

RF-04 (Venda).	O sistema deve registrar vendas associadas a um cliente.

RF-05.(Venda).	O sistema deve gerar um cupom fiscal após a venda. 

RF-06.(Estoque).	O sistema deve atualizar automaticamente o estoque após cada venda. 

RF-07.(Estoque).	O sistema deve emitir alertas quando o estoque de um produto estiver baixo. 

RF-08.(Relátorio).	O sistema deve gerar relatórios de vendas diárias, semanais e mensais. 

RF-09.(Relátorio).	O sistema deve gerar relatórios dos produtos mais vendidos. 

RF-010.(Relátorio).	O sistema deve gerar relatórios dos clientes mais frequentes. 

RF-011.(Cadastro).	O sistema deve permitir a autenticação de usuários (atendente ou administrador). 

RF-012.(Cadastro).	O sistema deve permitir que o administrador cadastre produtos e visualize o histórico completo de vendas.

RF-013(Pagamento). O sistema deve integrar-se com um sistema para processar o pagamento.

Requisitos Não Funcionais

RNF-01.(Usabilidade).	O sistema deve possuir uma interface amigável e fácil de utilizar pelos atendentes. 

RNF-02.(Seguraça).	O sistema deve garantir a segurança das informações dos clientes e do estoque. 

RNF-03.(Disponibilidade).	O sistema deve estar disponível para uso durante todo o horário de funcionamento da farmácia. 

RNF-04.(Desempenho).	O tempo de resposta para consultas de produtos deve ser inferior a 3 segundos. 

RNF-05.(Relátorio).	O sistema deve gerar relatórios em formato PDF.

RNF-06.(Acessibilidade).	O sistema deve permitir o acesso de diferentes usuários com permissões distintas (atendente e administrador). 

RNF-07.(Backup).	O sistema deve ser implementado de forma que permita futuras expansões (como integração com farmácias online).

# Diagrama de Atividades

![image](https://github.com/user-attachments/assets/ba754300-96ed-49ff-9d77-103aed0f30eb)


# Diagrama de Casos de Uso

![image](https://github.com/user-attachments/assets/a85d2e94-c420-412f-b8d6-28f6c0b3fb12)


# Descrição dos Casos de Uso
Caso de Uso: Realizar Cadastro
Ator Principal: Cliente


Ator Secundário: Atendente


Descrição:
O cliente chega até a loja e fornece suas informações e dados pessoais. O atendente solicita os dados e realiza o cadastro no sistema. Ao final do processo, o cliente passa a ter um perfil registrado.


Pré-condição:
O cliente não deve ter um cadastro prévio no sistema.


Pós-condição:
O cliente passa a possuir um perfil ativo no sistema.


Fluxo Principal:


O cliente chega à loja.


O atendente solicita os dados do cliente.


O cliente fornece os dados.


O atendente realiza o cadastro no sistema.


—------------------------------------------------------------------------------------------------------------------------


Caso de Uso: Realizar Compra
Ator Principal: Cliente


Ator Secundário: Atendente (Caixa)


Descrição:
O cliente seleciona os produtos desejados e se dirige ao caixa para efetuar o pagamento. O caixa escaneia os produtos, informa o valor ao cliente, valida o pagamento e aplica eventuais descontos. Após a finalização, o cliente recebe os produtos adquiridos.


Pré-condição:
O cliente deve possuir cadastro no sistema.


Pós-condição:
O cliente realiza a compra e recebe os produtos.


Fluxo Principal:


O cliente leva os produtos ao caixa.


O caixa escaneia os produtos e informa o valor ao cliente.


O cliente escolhe a forma de pagamento.


O caixa valida o pagamento e aplica os descontos.


O cliente sai da loja com os produtos.


—------------------------------------------------------------------------------------------------------------------------


Caso de Uso: Consulta de Estoque
Ator Principal: Atendente


Descrição:
O atendente acessa o sistema para verificar quais produtos estão disponíveis no estoque. O sistema exibe a lista atualizada com as quantidades disponíveis de cada item.


Pré-condição:
Os produtos precisam estar cadastrados e com as informações atualizadas no sistema.


Pós-condição:
O atendente obtém a informação sobre a disponibilidade dos produtos.


Fluxo Principal:


O atendente acessa o sistema e consulta o estoque.


O sistema exibe a lista de produtos disponíveis.


—------------------------------------------------------------------------------------------------------------------------


Caso de Uso: Atualiza Estoque
Ator Principal: Atendente


Descrição:
Quando há alterações nas quantidades dos produtos, o atendente acessa o sistema e realiza as modificações necessárias no estoque. Após as alterações, o sistema salva automaticamente os novos dados.


Pré-condição:
O estoque precisa ser ajustado devido a vendas, reposições ou perdas.


Pós-condição:
O estoque é atualizado com as quantidades corretas.


Fluxo Principal:


O atendente acessa o sistema e realiza as modificações no estoque.


O sistema salva as alterações feitas.


—------------------------------------------------------------------------------------------------------------------------


Caso de Uso: Alerta de Baixa Quantidade dos Produtos
Ator Principal: Atendente


Descrição:
Quando o estoque de determinado produto atinge um nível mínimo, o sistema envia automaticamente um alerta ao atendente. O atendente verifica a situação e decide se faz a reposição ou atualiza o estoque.


Pré-condição:
O estoque deve estar previamente atualizado.


Pós-condição:
O atendente é informado sobre a baixa quantidade e toma as ações necessárias para normalizar a situação.


Fluxo Principal:


O sistema envia um alerta ao atendente sobre a baixa quantidade de um produto.


O atendente verifica o estoque e decide entre atualizá-lo ou realizar o reabastecimento


# Diagrama de Sequência

![image](https://github.com/user-attachments/assets/89f35ddc-0016-4ad2-aff9-b5753cc884ff)


# Diagrama de Classes
![image](https://github.com/user-attachments/assets/52cff5fe-e74b-45d9-8fa9-182cd7ba4e7f)

# Diagrama de Estados

![image](https://github.com/user-attachments/assets/48dd7700-5e45-4f89-8c2e-b90b1fb47e9a)


# Diagrama de Implantação

![image](https://github.com/user-attachments/assets/e569b771-dcf8-4482-b3d9-8ab36d44bea2)


# Referências

*&lt;Lista de referências&gt;*
