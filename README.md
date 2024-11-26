# Engenharia de Software I (20242)
# Nome dos integrantes do grupo:
1) Érico Campos
2) Mario Fribel
3) Artur Zanoello
4) Lucas Sehn
5) Vinicius Franzzen

## Casos de uso do sistema de reserva de passagens aéreas
Tabelas com a descrição dos casos de uso
### Exemplo
![image](https://github.com/user-attachments/assets/41c6f615-98e4-44f5-8d5e-d22480685385)
# 
## Caso de Uso 1 - Autenticar cliente

| **Elemento**           | **Descrição**                                                                                                                                                                     |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Nome do Caso de Uso**| Autenticar cliente                                                                                                                                                    |
| **Escopo**             | Sistema de reservas de passagens aéreas                                                                                                                                            |
| **Nível**              | Sub-função                                                                                                                                                               |
| **Ator Principal**     | Cliente (Pessoa Física ou Jurídica)                                                                                                                                               |
| **Interessados e Interesses** | - **Sistema:** Necessita garantir que o cliente é autenticado antes de criar reservas. |
| **Pré-condições**      | - O cliente deve ter um cadastro prévio no sistema.                                                                      |
| **Garantias de Sucesso** | Cliente autenticado com sucesso.                                                                      |
| **Cenário de Sucesso** | 1. O cliente insere suas credenciais (login e senha). <br> 2. O sistema verifica as credenciais. <br> 3. O cliente é autenticado e tem acesso às funções de reserva. <br>  |
| **Extensões**          | - Caso o cliente insira credenciais incorretas, o sistema exibe mensagem de erro. <br>  - Após múltiplas tentativas incorretas, a conta pode ser temporariamente bloqueada.  |
| **Requisitos Especiais** | - Sistema deve garantir a segurança das informações de login e senha. |

## Caso de Uso 2 - Cancelar Reserva de Passagem

| **Elemento**           | **Descrição**                                                                                                                                                                     |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Nome do Caso de Uso**| Cancelar Reserva de Passagem                                                                                                                                                      |
| **Escopo**             | Sistema de Vendas de Passagens Aéreas                                                                                                                                             |
| **Nível**              | Objetivo do usuário                                                                                                                                                               |
| **Ator Principal**     | Cliente (Pessoa Física ou Jurídica)                                                                                                                                               |
| **Interessados e Interesses** | - **Cliente:** Deseja cancelar uma reserva de passagem aérea de forma simples e rápida. <br> - **Empresa de Táxi Aéreo:** Quer garantir que os cancelamentos sejam processados corretamente. |
| **Pré-condições**      | - O cliente deve estar autenticado no sistema. <br> - O cliente deve possuir uma reserva ativa.                                                                                     |
| **Garantias de Sucesso** | A reserva é cancelada e o cliente é informado sobre a política de reembolso.                                                                                                      |
| **Cenário de Sucesso** | 1. O cliente acessa o sistema de vendas de passagens aéreas. <br> 2. O cliente escolhe a opção de "Cancelar Reserva". <br> 3. O cliente insere o código da reserva. <br> 4. O sistema verifica a validade da reserva. <br> 5. O cliente confirma o cancelamento. <br> 6. O sistema cancela a reserva e atualiza o status no sistema. <br> 7. O cliente é notificado sobre o cancelamento e a política de reembolso via e-mail. |
| **Extensões**          | - **4a.** A reserva não é encontrada: <br> &nbsp;&nbsp;&nbsp;&nbsp;- **4a1.** O sistema informa que a reserva não foi encontrada e solicita a correção. <br> - **6a.** O sistema encontra um erro ao cancelar a reserva: <br> &nbsp;&nbsp;&nbsp;&nbsp;- **6a1.** O sistema exibe uma mensagem de erro e não cancela a reserva. |
| **Requisitos Especiais** | - O sistema deve criptografar informações sensíveis dos clientes. <br> - O sistema deve validar todas as informações inseridas pelo cliente. <br> - O sistema deve permitir o cancelamento de reservas dentro do prazo de 30 dias. |

## Caso de Uso 3 - Efetuar Pagamento de Reserva

| **Elemento**           | **Descrição**                                                                                                                                                                     |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Nome do Caso de Uso**| Efetuar Pagamento de Reserva                                                                                                                                                      |
| **Escopo**             | Sistema de Vendas de Passagens Aéreas                                                                                                                                             |
| **Nível**              | Objetivo do usuário                                                                                                                                                               |
| **Ator Principal**     | Cliente (Pessoa Física ou Jurídica)                                                                                                                                               |
| **Interessados e Interesses** | - **Cliente:** Deseja realizar o pagamento de uma reserva de passagem aérea de forma segura e rápida. <br> - **Empresa de Táxi Aéreo:** Quer garantir que os pagamentos sejam processados corretamente. |
| **Pré-condições**      | - O cliente deve estar autenticado no sistema. <br> - O cliente deve possuir uma reserva ativa e confirmada.                                                                                     |
| **Garantias de Sucesso** | O pagamento é processado com sucesso e a reserva é efetivada.                                                                                                                    |
| **Cenário de Sucesso** | 1. O cliente acessa o sistema de vendas de passagens aéreas. <br> 2. O cliente escolhe a opção de "Efetuar Pagamento". <br> 3. O cliente insere o código da reserva e escolhe o método de pagamento (cartão de crédito, pix ou boleto). <br> 4. O cliente insere os dados de pagamento. <br> 5. O sistema processa o pagamento. <br> 6. O sistema atualiza o status da reserva para efetivada. <br> 7. O cliente é notificado sobre a confirmação do pagamento via e-mail. |
| **Extensões**          | - **5a.** O pagamento é recusado: <br> &nbsp;&nbsp;&nbsp;&nbsp;- **5a1.** O sistema informa que o pagamento foi recusado e solicita a correção dos dados. <br> - **6a.** O sistema encontra um erro ao atualizar o status da reserva: <br> &nbsp;&nbsp;&nbsp;&nbsp;- **6a1.** O sistema exibe uma mensagem de erro e não efetiva a reserva. |
| **Requisitos Especiais** | - O sistema deve criptografar informações sensíveis dos clientes. <br> - O sistema deve validar todas as informações inseridas pelo cliente. <br> - O sistema deve permitir o pagamento em até 3 parcelas. |


## Diagrama de casos de uso
![Screenshot_1](https://github.com/user-attachments/assets/a8ff2bd0-e2a9-4c08-ad0f-1acdb6c77b81)

## Modelo de Domínio
Inserir nesta posição o modelo de domínio em formato JPG.
![image](https://github.com/user-attachments/assets/52fb0710-b1e1-4c2d-bd71-c4e09b8535fd)

## Diagrama de Atividades
Inserir nesta posição o diagrama de atividades em formato JPG.
![image](https://github.com/user-attachments/assets/e18391d4-530b-4012-9952-1f0357782732)

## Diagrama de Classes de Implementação
 Inserir nesta posição o diagrama de classes de Implementação em formato JPG---------
 
 ![image](https://github.com/user-attachments/assets/501e4f67-2f1e-402b-b54e-44956731630a).


![image](https://github.com/user-attachments/assets/9041d4c8-7ec5-47c7-a285-ebd9906ca79e)

