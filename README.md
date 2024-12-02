# Engenharia de Software I (2024)
# Nome dos integrantes do grupo:
1) Érico Campos
2) Mario Fribel
3) Artur Zanoello
4) Lucas Sehn
5) Vinicius Franzzen

## Casos de uso do sistema de reserva de passagens aéreas
Tabelas com a descrição dos casos de uso

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

## Caso de Uso 2 - Consultar Voos Disponíveis

| **Elemento**           | **Descrição**                                                                                                                                                                     |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Nome do Caso de Uso**| Consultar Voos Disponíveis                                                  |
| **Escopo**             | Sistema de reservas de passagens aéreas                                     |
| **Nível**              | Sub-função                                                                  |
| **Ator Principal**     | Cliente                                                                     |
| **Interessados e Interesses**| Cliente: Deseja visualizar os voos disponíveis antes de fazer a reserva.       |
| **Pré-condições**      | O cliente deve estar autenticado.                                           |
| **Garantias de Sucesso**| Cliente visualiza lista de voos disponíveis para seleção.                   |
| **Cenário de Sucesso**  | 1. O cliente acessa a funcionalidade de consulta de voos. <br> 2. Define critérios (origem, destino, data). <br> 3. O sistema exibe voos disponíveis com detalhes (horário, quilometragem, etc.).|
| **Extensões**           | - Caso não haja voos disponíveis, o sistema informa o cliente.              |
| **Requisitos Especiais**| Sistema deve ter acesso a informações atualizadas dos voos.                 |

## Caso de Uso 3 - Fazer Reserva de Passagem Aérea

| **Elemento**           | **Descrição**                                                                                                                                                                     |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Nome do Caso de Uso**    | Fazer Reserva de Passagem Aérea                                             |
| **Escopo**                 | Sistema de reservas de passagens aéreas para táxi aéreo                    |
| **Nível**                  | Objetivo do usuário                                                        |
| **Ator Principal**         | Cliente (Pessoa Física ou Jurídica) autenticado no sistema.                |
| **Interessados e Interesses** | Cliente: Deseja reservar uma passagem aérea para um voo específico.           |
| **Pré-condições**          | O cliente deve estar cadastrado e autenticado no sistema.                  |
| **Garantias de Sucesso**   | Reserva criada com um código único, com todos os dados necessários confirmados.|
| **Cenário de Sucesso**     | 1. O cliente acessa o sistema e se autentica. <br> 2. Escolhe o voo desejado (origem, destino, data e horário). <br> 3. Seleciona a aeronave e o assento disponível. <br> 4. O sistema gera um código de reserva. <br>                           5. A reserva é criada e fica disponível para confirmação ou alteração.      |
| **Extensões**              | - Caso o cliente deseje cancelar a reserva, o sistema permite o cancelamento. <br> - Reserva não confirmada em 30 dias é automaticamente cancelada.           |
| **Requisitos Especiais**   | Sistema deve ser capaz de armazenar dados do cliente e informações do voo.  |

## Caso de Uso 4 - Efetuar Pagamento de Reserva 

| **Elemento**           | **Descrição**                                                                                                                                                                     |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Nome do Caso de Uso**    | Efetuar Pagamento de Reserva                                                |
| **Escopo**                 | Sistema de reservas de passagens aéreas                                     |
| **Nível**                  | Sub-função                                                                  |
| **Ator Principal**         | Cliente                                                                     |
| **Interessados e Interesses** | Cliente: Deseja garantir sua passagem e efetuar o pagamento.                   |
| **Pré-condições**          | A reserva deve ter sido previamente criada.                                |
| **Garantias de Sucesso**   | Reserva confirmada e pagamento registrado no sistema.                      |
| **Cenário de Sucesso**     | 1. O cliente seleciona uma reserva para confirmação. <br> 2. Escolhe o método de pagamento (cartão, PIX, boleto). <br> 3. Efetua o pagamento. <br> 4. O sistema atualiza o status da reserva para 'confirmada'.               |
| **Extensões**              | - Caso o pagamento não seja concluído, a reserva permanece como 'pendente'.|
| **Requisitos Especiais**   | O sistema deve integrar-se com os meios de pagamento.                      |

## Caso de Uso 5 - Gerar Venda de Passagem Aérea 

| **Elemento**           | **Descrição**                                                                                                                                                                     |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Nome do Caso de Uso**    | Gerar Venda de Passagem Aérea                                               |
| **Escopo**                 | Sistema de reservas de passagens aéreas                                     |
| **Nível**                  | Objetivo do usuário                                                        |
| **Ator Principal**         | Cliente                                                                     |
| **Interessados e Interesses** | Cliente: Deseja ter a passagem garantida após a confirmação da reserva.        |
| **Pré-condições**          | A reserva deve estar confirmada.                                           |
| **Garantias de Sucesso**   | Venda registrada e passagem emitida para o cliente.                        |
| **Cenário de Sucesso**     | 1. O sistema identifica a reserva confirmada. <br> 2. Gera a passagem e registra a venda.                                     |
| **Extensões**              | - Em caso de cancelamento após venda, aplicar regras de reembolso.         |
| **Requisitos Especiais**   | O sistema deve emitir um comprovante de venda e envio ao cliente.          |

## Caso de Uso 6 - Cancelar Reserva de Passagem Aérea 

| **Elemento**           | **Descrição**                                                                                                                                                                     |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Nome do Caso de Uso**    | Cancelar Reserva de Passagem Aérea                                          |
| **Escopo**                 | Sistema de reservas de passagens aéreas                                     |
| **Nível**                  | Sub-função                                                                  |
| **Ator Principal**         | Cliente                                                                     |
| **Interessados e Interesses** | Cliente: Pode cancelar a reserva dentro do prazo de 30 dias.                   |
| **Pré-condições**          | A reserva deve estar criada e dentro do prazo de validade.                  |
| **Garantias de Sucesso**   | Reserva cancelada e, se aplicável, reembolso parcial do pagamento.           |
| **Cenário de Sucesso**     | 1. O cliente seleciona a reserva para cancelamento. <br> 2. O sistema verifica se está no prazo de cancelamento. <br> 3. A reserva é cancelada, e o status é atualizado.                          |
| **Extensões**              | - Se a reserva estiver fora do prazo de cancelamento, o sistema informa o cliente.|
| **Requisitos Especiais**   | Sistema deve processar devolução parcial caso o pagamento já tenha sido feito.|

## Caso de Uso 7 - Cadastrar Voos 

| **Elemento**           | **Descrição**                                                                                                                                                                     |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Nome do Caso de Uso**    | Cadastrar Voos                                                              |
| **Escopo**                 | Sistema de reservas de passagens aéreas                                     |
| **Nível**                  | Função principal                                                            |
| **Ator Principal**         | Companhia aérea                                                             |
| **Interessados e Interesses** | O administrador deseja adicionar voos à grade.                                |
| **Pré-condições**          | O administrador deve estar autenticado.                                     |
| **Garantias de Sucesso**   | O voo é registrado no sistema com todos os dados necessários.               |
| **Cenário de Sucesso**     | 1. O administrador acessa a opção 'Cadastrar Voo'. <br> 2. Insere as informações do voo (código, origem, destino, horários, quilometragem). <br> 3. O sistema salva o novo voo.                                              |
| **Extensões**              | Caso faltem dados obrigatórios, o sistema solicita correções.              |
| **Requisitos Especiais**   | O sistema deve permitir o cadastro de voos apenas por administradores autenticados, validar os dados inseridos e registrar as ações em um log de auditoria.|

## Caso de Uso 8 - Gerenciar Cancelamento de Voos

| **Elemento**           | **Descrição**                                                                                                                                                                     |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Nome do Caso de Uso**    | Gerenciar Cancelamento de Voos                                              |
| **Escopo**                 | Sistema de reservas de passagens aéreas                                     |
| **Nível**                  | Função principal                                                            |
| **Ator Principal**         | Companhia aérea                                                             |
| **Interessados e Interesses** | A companhia aérea deseja cancelar voos por motivos operacionais.              |
| **Pré-condições**          | O voo precisa estar programado no sistema.                                 |
| **Garantias de Sucesso**   | O voo é cancelado e os clientes são notificados.                            |
| **Cenário de Sucesso**     | 1. O administrador acessa a opção 'Cancelar Voo'. <br> 2. Seleciona o voo que deseja cancelar. <br> 3. Informa o motivo do cancelamento. <br> 4. O sistema atualiza o status do voo para 'Cancelado' e notifica os clientes.|
| **Extensões**              | Caso o voo já tenha reservas confirmadas, o sistema gera alertas e opções para reembolso.|
| **Requisitos Especiais**   | Notificar automaticamente os clientes afetados pelo cancelamento e atender às regulamentações sobre direitos dos passageiros.|

## Caso de Uso 9 - Receber Escala de Voos 

| **Elemento**           | **Descrição**                                                                                                                                                                     |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Nome do Caso de Uso**    | Receber Escala de Voos                                                     |
| **Escopo**                 | Sistema de reservas de passagens aéreas                                     |
| **Nível**                  | Sub-função                                                                  |
| **Ator Principal**         | Piloto                                                                      |
| **Interessados e Interesses** | O piloto precisa saber sua escala de voos para planejamento.                   |
| **Pré-condições**          | O piloto deve estar autenticado no sistema.                                |
| **Garantias de Sucesso**   | A escala de voos do piloto é exibida corretamente.                         |
| **Cenário de Sucesso**     | 1. O piloto autentica-se no sistema. <br> 2. Seleciona a opção 'Consultar Escala'. <br> 3. O sistema exibe os voos programados para o piloto.                     |
| **Extensões**              | Caso não haja voos programados, o sistema exibe uma mensagem apropriada.   |
| **Requisitos Especiais**   | O sistema deve atualizar a escala de voos em tempo real, garantir acesso exclusivo a pilotos autenticados e notificar automaticamente sobre alterações.|

## Caso de Uso 10 - Gerenciar Confirmação de Voos

| **Elemento**           | **Descrição**                                                                                                                                                                     |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Nome do Caso de Uso**    | Gerenciar Confirmação de Voos                                               |
| **Escopo**                 | Sistema de reservas de passagens aéreas                                     |
| **Nível**                  | Função principal.                                                                 |
| **Ator Principal**         | Companhia aérea                                                             |
| **Interessados e Interesses** | A companhia aérea deseja confirmar voos por motivos operacionais.        |
| **Pré-condições**          | O voo precisa estar programado no sistema.                                 |
| **Garantias de Sucesso**   | O voo é confirmado e os clientes são notificados.                                       |
| **Cenário de Sucesso**     | 1. O administrador acessa a opção "Confirmar Voo". <br> 2. Seleciona o voo que deseja confirmar. <br> 3. O sistema atualiza o status do voo para ‘Confirmado’ e notifica os clientes.                                        |
| **Extensões**              | Avisa os clientes que o voo foi confirmado.   |
| **Requisitos Especiais**   | Apenas administradores autenticados possam gerenciar confirmações de voos.|

## Caso de Uso 11 - Gerenciar Frota de Aeronaves

| **Elemento**           | **Descrição**                                                                                                                                                                     |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Nome do Caso de Uso**    | Gerenciar Frota de Aeronaves                                            |
| **Escopo**                 | Sistema de reservas de passagens aéreas                                     |
| **Nível**                  | Sub-função                                                           |
| **Ator Principal**         | Companhia aérea                                                             |
| **Interessados e Interesses** | A companhia aérea deseja manter atualizados os registros de aeronaves.             |
| **Pré-condições**          | O administrador deve estar autenticado.                                |
| **Garantias de Sucesso**   | A frota é gerenciada corretamente.                        |
| **Cenário de Sucesso**     | 1. O administrador acessa a opção "Gerenciar Frota". <br> 2. Insere, edita ou remove dados das aeronaves (registro, tipo, assentos). <br> 3. O sistema salva as alterações.|
| **Extensões**              | Caso faltem informações obrigatórias, o sistema exibe mensagens de erro.                             |
| **Requisitos Especiais**   | O sistema deve permitir apenas administradores autenticados para gerenciar aeronaves   |

## Diagrama de casos de uso
![Sistema_de_reservas_aereas_B](https://github.com/user-attachments/assets/01a0c343-5f85-4b92-9ac1-fec39132e9df)

## Modelo de Domínio
![viagens_C](https://github.com/user-attachments/assets/5c0281e0-14cc-49af-b66a-ac05683ad9b6)

## Diagrama de Atividades
![viagens D](https://github.com/user-attachments/assets/a5f75582-f42b-40e0-aea9-4e9dcf94d2bd)

## Diagrama de Classes de Implementação
![viagens_E](https://github.com/user-attachments/assets/aad13d0f-df75-4626-804e-b0400ba9deba)


