# Simulador de sistema

Simulação interativa do atendimento de uma clínica ambulatorial pelo WhatsApp. É uma página única (`index.html`), sem dependências nem build: basta abrir no navegador.

A página mostra uma conversa de WhatsApp ao lado de um painel interno com:

- **Fluxo n8n:** cada etapa executada (mensagem recebida, regras, consulta ao ProDoctor, resposta do Grok).
- **Agenda ProDoctor:** horários do dia, com as janelas reservadas a primeiros clientes.
- **Convênios:** matriz de cobertura por especialidade.
- **Recepção:** conversa transferida para as secretárias, com a automação pausada.

## Regras simuladas

- Identificação com dois dados que batem: CPF ou nome completo, mais a data de nascimento. Se mais de um cadastro bater, o atendimento vai para a recepção.
- Matriz de convênios e especialidades, com oferta de atendimento particular ou recepção quando o convênio não cobre.
- Os 4 últimos horários da manhã e os 4 últimos da tarde ficam reservados a primeiros clientes.
- Perguntas clínicas são recusadas. Clique para ligar e transbordo para a recepção.

## Aviso

Não há integração real. As respostas vêm de regras locais, e os CPFs, as datas de nascimento, a agenda e o telefone são fictícios. No sistema de verdade, o Grok interpreta e redige, e o n8n aplica as regras e acessa o ProDoctor.
