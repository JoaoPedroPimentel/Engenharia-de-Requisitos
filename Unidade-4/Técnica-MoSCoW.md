A técnica **MoSCoW** organiza os requisitos de acordo com a prioridade de implementação:

- **Must Have (M):** obrigatório e indispensável para a primeira versão.
- **Should Have (S):** importante, mas pode ser adiado sem impedir o funcionamento principal.
- **Could Have (C):** desejável e pode ser implementado se houver tempo e recursos.
- **Won't Have Now (W):** não será implementado nesta primeira entrega, podendo ficar para uma versão futura.

## Matriz MoSCoW – Requisitos Funcionais

| **ID** | **Requisito** | **M** | **S** | **C** | **W** | **Justificativa** |
|:---:|---|:---:|:---:|:---:|:---:|---|
| RF01 | Cadastrar pacientes | X | | | | Essencial para identificar o paciente. |
| RF02 | Consultar e atualizar pacientes | X | | | | Mantém os dados corretos e atualizados. |
| RF03 | Cadastrar médicos | X | | | | Necessário para organizar os profissionais. |
| RF04 | Cadastrar especialidades | X | | | | Permite organizar e localizar os médicos. |
| RF05 | Cadastrar horários dos médicos | X | | | | Fundamental para controlar a agenda. |
| RF06 | Consultar horários disponíveis | X | | | | Necessário para realizar o agendamento. |
| RF07 | Realizar agendamentos | X | | | | É uma função central do sistema. |
| RF08 | Impedir conflitos de horários | X | | | | Evita dois pacientes no mesmo horário. |
| RF09 | Cancelar consultas | X | | | | Libera horários e mantém a agenda correta. |
| RF10 | Reagendar consultas | | X | | | Importante, mas pode ser implementado depois. |
| RF11 | Enviar confirmação | X | | | | Reduz falhas de comunicação. |
| RF12 | Enviar lembretes | | X | | | Ajuda a reduzir faltas. |
| RF13 | Registrar presença ou falta | X | | | | Permite controlar o comparecimento. |
| RF14 | Registrar atendimento médico | X | | | | Fundamental para concluir o atendimento. |
| RF15 | Indicadores de desempenho | | X | | | Apoia a gestão, mas não é essencial no início. |

## Matriz MoSCoW – Requisitos Não Funcionais

| **ID** | **Requisito** | **M** | **S** | **C** | **W** | **Justificativa** |
|:---:|---|:---:|:---:|:---:|:---:|---|
| RNF01 | Horários disponíveis em até 3 segundos | X | | | | Garante agilidade no atendimento. |
| RNF02 | Autenticação para usuários administrativos | X | | | | Protege o acesso ao sistema. |
| RNF03 | Interface simples e intuitiva | | X | | | Facilita o uso pelos funcionários. |
| RNF04 | Disponibilidade durante o horário da clínica | X | | | | O sistema precisa estar disponível quando a clínica atende. |
| RNF05 | Evitar perda de dados | X | | | | Evita prejuízos e perda de informações. |
| RNF06 | Proteção dos dados pessoais | X | | | | Protege informações dos pacientes. |
| RNF07 | Agendamento processado em até 3 segundos | | X | | | Melhora a eficiência do processo. |
| RNF08 | Controle de acesso por perfil | X | | | | Evita acesso indevido às funções. |
| RNF09 | Mensagens claras de erro e confirmação | | X | | | Facilita a compreensão do usuário. |
| RNF10 | Compatibilidade com principais navegadores | | X | | | Facilita o acesso em diferentes equipamentos. |

## Parte A - Selecionar 5 requisitos indispensáveis

| Ordm | MoSCoW | ID | Requisito | Por que precisa permanecer? |
|------|--------|----|-----------|-----------------------------|
| 1 | M | RF01 | O sistema deverá permitir cadastrar pacientes. | Sem o cadastro dos pacientes, não é possível realizar o agendamento das consultas. |
| 2 | M | RF03 | O sistema deverá permitir cadastrar médicos. | É necessário para identificar quais médicos realizarão os atendimentos. |
| 3 | M | RF05 | O sistema deverá permitir cadastrar horários de atendimento dos médicos. | Os horários são necessários para organizar a disponibilidade dos médicos. |
| 4 | M | RF07 | O sistema deverá permitir realizar agendamentos. | É uma das principais funcionalidades do sistema, permitindo marcar consultas. |
| 5 | M | RF08 | O sistema deverá impedir dois agendamentos para o mesmo médico e horário. | Evita conflitos e garante que não ocorram dois agendamentos no mesmo horário. |

## Parte B - Selecionar 3 requisitos que podem ir para uma versão futura

| MoSCoW | ID | Requisito | Impacto de adiar |
|--------|----|-----------|------------------|
| C | RF11 | O sistema deverá enviar confirmação do agendamento. | O agendamento continuará funcionando, mas sem confirmação automática ao paciente. |
| C | RF12 | O sistema deverá enviar lembretes das consultas. | As consultas poderão ser realizadas, porém os pacientes não receberão lembretes. |
| W | RF15 | O sistema deverá disponibilizar indicadores de desempenho. | A clínica ficará sem indicadores na primeira versão, mas o funcionamento principal do sistema não será prejudicado. |
## Resumo da Priorização

### Must Have – Obrigatórios

- RF01, RF02, RF03, RF04, RF05, RF06, RF07, RF08, RF09, RF11, RF13 e RF14.
- RNF01, RNF02, RNF04, RNF05, RNF06 e RNF08.

### Should Have – Importantes

- RF10, RF12 e RF15.
- RNF03, RNF07, RNF09 e RNF10.

### Could Have – Desejáveis

- Aplicativo para pacientes;
- Pesquisa de satisfação;
- Lista de espera automatizada;
- Integração com outros sistemas.

### Won't Have Now – Não será implementado inicialmente

- Gestão financeira completa;
- Controle de estoque;
- Integração com planos de saúde;
- Prontuário eletrônico completo com funcionalidades avançadas.

### Justificativa de cinco decisões

**1. RF07 – Agendamento → Must Have**  
É uma das principais funções do sistema e atende diretamente ao problema central da clínica.

**2. RF08 – Prevenção de conflitos → Must Have**  
Resolve diretamente um dos principais problemas atuais.

**3. RF11 – Confirmação → Must Have**  
Reduz falhas de comunicação com os pacientes.

**4. RF12 – Lembretes → Should Have**  
É importante para reduzir faltas, mas o processo básico pode funcionar sem essa funcionalidade na primeira versão.

**5. RF15 – Indicadores → Should Have**  
É importante para a gestão e melhoria contínua, mas pode ser implementado após as funcionalidades essenciais.

**Alunos: João Pedro Pimentel,
Nicolle,
Arthur,
Sara**

Link da Atividade completa: https://github.com/marcopopovidis-coder/engenharia_software_moscow_repo/edit/main/Atividade_Completa_Original_MoSCoW_Adicionado.md
