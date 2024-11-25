# Engenharia de Software I (20242)
# Nome dos integrantes do grupo:
1) Érico Campos
2) Mario Fribel
3) Artur Zanoello
4) Lucas Sehn
5) Vinicius Franzzen

## Casos de uso do sistema de reserva de passagens aéreas
Tabelas com a descrição dos casos de uso

| **Elemento**           | **Descrição**                                                                                                                                                                     |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Nome do Caso de Uso**| Gerenciar Reserva de Passagem                                                                                                                                                     |
| **Escopo**             | Sistema de Vendas de Passagens Aéreas                                                                                                                                             |
| **Nível**              | Objetivo do usuário                                                                                                                                                               |
| **Ator Principal**     | Cliente (Pessoa Física ou Jurídica)                                                                                                                                               |
| **Interessados e Interesses** | - **Cliente:** Deseja realizar uma reserva de passagem aérea de forma fácil e rápida. <br> - **Empresa de Táxi Aéreo:** Quer garantir que as reservas sejam feitas e gerenciadas eficientemente. |
| **Pré-condições**      | - O cliente deve estar autenticado no sistema. <br> - O cliente deve possuir um cadastro válido no sistema.                                                                        |
| **Garantias de Sucesso** | A reserva é registrada com um código único e os detalhes da viagem são armazenados corretamente no sistema.                                                                       |
| **Cenário de Sucesso** | 1. O cliente acessa o sistema de vendas de passagens aéreas. <br> 2. O cliente escolhe a opção de "Fazer Reserva". <br> 3. O cliente seleciona o voo desejado informando origem, destino, data e horário. <br> 4. O cliente insere os dados do passageiro (identificação, nome, CPF, etc.). <br> 5. O cliente seleciona a aeronave e o assento desejado. <br> 6. O sistema gera um código de reserva e exibe uma mensagem de confirmação. <br> 7. A reserva é armazenada no sistema e o cliente é notificado via e-mail. |
| **Extensões**          | - **3a.** O cliente seleciona um voo que está cheio: <br> &nbsp;&nbsp;&nbsp;&nbsp;- **3a1.** O sistema informa que o voo está lotado e sugere voos alternativos. <br> - **4a.** O cliente insere informações inválidas: <br> &nbsp;&nbsp;&nbsp;&nbsp;- **4a1.** O sistema exibe uma mensagem de erro e solicita a correção. <br> - **6a.** O sistema encontra um erro ao gerar o código de reserva: <br> &nbsp;&nbsp;&nbsp;&nbsp;- **6a1.** O sistema exibe uma mensagem de erro e não salva a reserva. |
| **Requisitos Especiais** | - O sistema deve criptografar informações sensíveis dos clientes. <br> - O sistema deve validar todas as informações inseridas pelo cliente. <br> - O sistema deve permitir a alteração, confirmação ou cancelamento de reservas dentro do prazo de 30 dias. |

Elemento	Descrição
Nome do Caso de Uso	Cancelar Reserva de Passagem
Escopo	Sistema de Vendas de Passagens Aéreas
Nível	Objetivo do usuário
Ator Principal	Cliente (Pessoa Física ou Jurídica)
Interessados e Interesses	- Cliente: Deseja cancelar uma reserva de passagem aérea de forma simples e rápida. <br> - Empresa de Táxi Aéreo: Quer garantir que os cancelamentos sejam processados corretamente.
Pré-condições	- O cliente deve estar autenticado no sistema. <br> - O cliente deve possuir uma reserva ativa.
Garantias de Sucesso	A reserva é cancelada e o cliente é informado sobre a política de reembolso.
Cenário de Sucesso	1. O cliente acessa o sistema de vendas de passagens aéreas. <br> 2. O cliente escolhe a opção de "Cancelar Reserva". <br> 3. O cliente insere o código da reserva. <br> 4. O sistema verifica a validade da reserva. <br> 5. O cliente confirma o cancelamento. <br> 6. O sistema cancela a reserva e atualiza o status no sistema. <br> 7. O cliente é notificado sobre o cancelamento e a política de reembolso via e-mail.
Extensões	- 4a. A reserva não é encontrada: <br> &nbsp;&nbsp;&nbsp;&nbsp;- 4a1. O sistema informa que a reserva não foi encontrada e solicita a correção. <br> - 6a. O sistema encontra um erro ao cancelar a reserva: <br> &nbsp;&nbsp;&nbsp;&nbsp;- 6a1. O sistema exibe uma mensagem de erro e não cancela a reserva.
Requisitos Especiais	- O sistema deve criptografar informações sensíveis dos clientes. <br> - O sistema deve validar todas as informações inseridas pelo cliente. <br> - O sistema deve permitir o cancelamento de reservas dentro do prazo de 30 dias.

![image](https://github.com/user-attachments/assets/41c6f615-98e4-44f5-8d5e-d22480685385)

## Diagrama de casos de uso
Inserir nesta posição o diagrama de casos de uso em formato JPG.
![image](https://github.com/user-attachments/assets/c5d06f7e-5ebf-4514-92a8-298d01401226)

## Modelo de Domínio
Inserir nesta posição o modelo de domínio em formato JPG.
![image](https://github.com/user-attachments/assets/52fb0710-b1e1-4c2d-bd71-c4e09b8535fd)

## Diagrama de Atividades
Inserir nesta posição o diagrama de atividades em formato JPG.
![image](https://github.com/user-attachments/assets/e18391d4-530b-4012-9952-1f0357782732)

## Diagrama de Classes de Implementação
 Inserir nesta posição o diagrama de classes de Implementação em formato JPG.
![image](https://github.com/user-attachments/assets/501e4f67-2f1e-402b-b54e-44956731630a).
....

![image](https://github.com/user-attachments/assets/9041d4c8-7ec5-47c7-a285-ebd9906ca79e)

