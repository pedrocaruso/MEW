<h2><a href= "https://www.mackenzie.br">Universidade Presbiteriana Mackenzie</a></h2>
<h3><a href= "https://www.mackenzie.br/graduacao/sao-paulo-higienopolis/sistemas-de-informacao">Sistemas de Informação</a></h3>


<font size="+12"><center>
# Sistema de Gestão para a Farmácia Vida Saudável
</center></font>

>*Observação 1: A estrutura inicial deste documento é só um exemplo. O seu grupo deverá alterar esta estrutura de acordo com o que está sendo solicitado na disciplina.*

>*Observação 2: O índice abaixo não precisa ser editado se você utilizar o Visual Studio Code com a extensão **Markdown All in One**. Essa extensão atualiza o índice automaticamente quando o arquivo é salvo.*

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

* Kauan Sarzi Da Rocha


# Descrição do Projeto

Este projeto é um software para a Farmácia Vida Saudável, um estabelecimento de pequeno porte que busca modernizar e otimizar sua gestão interna. O sistema permitirá o controle eficiente de vendas, estoque, cadastro de clientes e geração de relatórios gerenciais, substituindo os processos manuais atualmente utilizados. O sistema atende tanto às demandas operacionais dos atendentes quanto às necessidades administrativas do gestor da farmácia, garantindo agilidade, organização e precisão no atendimento ao cliente.

# Análise de Requisitos Funcionais e Não-Funcionais

## Requisitos Funcionais

### RF-01 – Cadastro de Clientes  
O sistema deve permitir o **cadastro**, **edição** e **exclusão** de clientes, incluindo informações como **nome**, **CPF**, **endereço** e **telefone**.

### RF-02 – Cadastro de Produtos  
O sistema deve permitir o **cadastro**, **edição** e **exclusão** de produtos, incluindo **nome**, **descrição**, **lote**, **data de validade** e **quantidade em estoque**.

### RF-03 – Realização de Vendas  
O sistema deve possibilitar a **realização de vendas**, associando um **cliente** e os **produtos comprados**, gerando um **recibo digital**.

### RF-04 – Cálculo de Compra  
O sistema deve **calcular automaticamente** o **total da compra** e aplicar **descontos promocionais**, caso necessário.

### RF-05 – Histórico de Compras  
O sistema deve permitir a **consulta do histórico de compras** dos clientes cadastrados.

### RF-06 – Alerta de Validade  
O sistema deve emitir **alertas para produtos próximos da data de validade**.

### RF-07 – Controle de Estoque  
O sistema deve permitir o **controle de estoque**, informando a **quantidade disponível** de cada produto.

### RF-08 – Relatórios de Vendas  
O sistema deve permitir a **geração de relatórios de vendas** **diárias**, **semanais** e **mensais**.

### RF-09 – Busca de Produtos  
O sistema deve permitir a **busca por produtos no estoque**, pelo **nome** ou **código de barras**.

### RF-10 – Integração com Pagamentos  
O sistema deve integrar-se com um **sistema de pagamento** para processar **cartões de crédito e débito**.
<br><br>

## Requisitos Não Funcionais

### RNF-01 – Disponibilidade  
O sistema deve estar disponível **99,9% do tempo**, garantindo **alta disponibilidade**.

### RNF-02 – Desempenho  
O **tempo de resposta** para a **consulta de produtos no estoque** não deve ultrapassar **2 segundos**.

### RNF-03 – Acessibilidade  
O sistema deve ser acessível via **navegador web** e **aplicativo móvel**.

### RNF-04 – Segurança e Conformidade  
Os **dados dos clientes** e das **transações** devem ser armazenados de forma segura, garantindo **conformidade com a LGPD** (Lei Geral de Proteção de Dados).

### RNF-05 – Autenticação  
O sistema deve exigir **autenticação dos funcionários** para acesso às **funções administrativas**.

### RNF-06 – Criptografia  
O **banco de dados** deve ser protegido com **criptografia**, evitando **acessos não autorizados**.

### RNF-07 – Escalabilidade  
O sistema deve suportar até **500 usuários simultâneos** sem degradação no desempenho.

### RNF-08 – Backup  
O sistema deve realizar **backups automáticos diariamente**.

### RNF-09 – Usabilidade  
A **interface do usuário** deve ser **intuitiva** e **responsiva**, adaptando-se a **diferentes dispositivos**.

### RNF-10 – Auditoria e Log  
O sistema deve permitir **auditoria de todas as transações realizadas**.  
Os **logs devem ser armazenados por no mínimo 5 anos** e protegidos contra **alteração ou exclusão**.

<br><br>





# Diagrama de Atividades

![Captura de tela 2025-03-20 163355](https://github.com/user-attachments/assets/fabe74d8-1ca6-41f4-b3da-ad531041c2ea) <br><br>



# Diagrama de Casos de Uso

![image](https://github.com/user-attachments/assets/21f57de6-4748-43af-80b2-9a790748874c)
 <br><br>


# Descrição dos Casos de Uso

##  Caso de Uso: Cadastrar Produto
- **Ator:** Administrador  
- **Descrição:** Permite ao administrador cadastrar novos medicamentos e produtos no sistema, informando nome, descrição, fabricante, lote, validade, quantidade em estoque e preço de venda.  
- **Pré-condição:** O administrador deve estar autenticado no sistema 
- **Pós-condição:** Produto registrado com sucesso e disponível para consulta 
- **Fluxo Principal:**
  1. Admin acessa o menu de cadastro
  2. Preenche os campos obrigatórios
  3. salva as informações
  4. sistema confirma o cadastro
- **Fluxo Alternativo:** Campos obrigatórios em branco : sistema exibe mensagem de erro

<br>

##  Caso de Uso: Consultar Produto
- **Ator:** Atendente  
- **Descrição:** Permite que o atendente busque por um medicamento ou produto para verificar sua disponibilidade 
- **Pré-condição:** O atendente deve estar autenticado  
- **Pós-condição:** Produto localizado e informações exibidas 
- **Fluxo Principal:**
  1. Atendente insere nome ou código do produto
  2. Sistema retorna dados do produto, incluindo estoque  
- **Fluxo Alternativo:** Produto não encontrado = sistema exibe "produto indisponível"

<br>

##  Caso de Uso: Registrar Venda
- **Ator:** Atendente  
- **Descrição:** Realiza o processo de venda de um ou mais produtos a um cliente, vinculando ao CPF 
- **Pré-condição:** Produto deve estar disponivel em estoque 
- **Pós-condição:** Estoque atualizado, venda registrada e cupom gerado  
- **Fluxo Principal:**
  1. Atendente seleciona produtos
  2. Informa CPF do cliente
  3. Sistema registra venda
  4. Estoque é atualizado automaticamente
  5. Cupom fiscal é gerado

<br>

##  Caso de Uso: Cadastrar Cliente
- **Ator:** Atendente  
- **Descrição:** Registra os dados de um novo cliente no sistema
- **Pré-condição:** CPF do cliente deve ser válido e unico  
- **Pós-condição:** Cliente salvo com histórico de compras em branco 
- **Fluxo Principal:**
  1. Atendente acessa o menu de cadastro
  2. Insere nome, CPF e telefone
  3. Sistema salva os dados  
- **Fluxo Alternativo:** CPF já cadastrado = sistema exibe erro de duplicidade

<br>

##  Caso de Uso: Gerar Relatórios
- **Ator:** Administrador  
- **Descrição:** Permite gerar relatórios de vendas, estoque e comportamento de clientes 
- **Pré-condição:** Acesso de administrador  
- **Pós-condição:** Relatório exibido na tela ou exportado
- **Fluxo Principal:**
  1. Administrador escolhe tipo de relatório (vendas, produtos ou clientes)
  2. Informa período desejado
  3. Sistema gera o relatório com os dados solicitados 

<br>

##  Caso de Uso: Autenticar Usuário
- **Ator:** Administrador ou Atendente  
- **Descrição:** Realiza login no sistema com credenciais e define permissões de acesso 
- **Pré-condição:** Usuário deve possuir login e senha validos  
- **Pós-condição:** Usuário acessa as funções conforme seu perfil 
- **Fluxo Principal:**
  1. Usuário informa login e senha
  2. Sistema valida credenciais
  3. Libera acesso ao ambiente correspondente admin ou atendente
- **Fluxo Alternativo:** Dados invalidos = sistema bloqueia acesso e exibe aviso

<br>


# Diagrama de Sequência

*&lt;Diagrama de ordem e interação dos objetos&gt;*

# Diagrama de Classes

*&lt;Diagrama de relacionamento entre classes para os seus atributos e operações&gt;*

# Diagrama de Estados

![image](https://github.com/user-attachments/assets/04e0e1e5-2245-4910-9a48-b8f780e067ab)



# Diagrama de Implantação

![image](https://github.com/user-attachments/assets/aa099b9a-f891-4388-9c02-4834f199ec53)


# Referências

*&lt;Lista de referências&gt;*
