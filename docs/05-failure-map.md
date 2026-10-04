# 05. Service Failure Map

## Objetivo
Mapear falhas do serviço para identificar relação entre causa, impacto e consequência operacional.

## Estrutura
Service Failure → Root Cause → User Impact → Operational Impact

## Exemplos

### Caso 1: usuário legítimo bloqueado
- Service failure: operação bloqueada sem explicação clara
- Root cause: regra excessivamente rígida
- User impact: frustração, insegurança, abandono
- Operational impact: aumento de contato com suporte e revisão manual

### Caso 2: mensagem genérica
- Service failure: mensagem genérica e sem contexto
- Root cause: contexto limitado da decisão
- User impact: confusão e desconfiança
- Operational impact: múltiplos contatos repetidos e escalonamento

### Caso 3: suporte sem contexto
- Service failure: atendimento incapaz de explicar a decisão
- Root cause: sistemas desconectados ou dados incompletos
- User impact: sensação de injustiça e falta de controle
- Operational impact: escalonamento e retrabalho

### Caso 4: revisão manual demorada
- Service failure: demora na análise do caso
- Root cause: processo fragmentado e manual
- User impact: abandono e perda de confiança
- Operational impact: custo operacional e pressão sobre a operação

### Caso 5: reversão não propagada
- Service failure: caso reprocessado sem correção completa do bloqueio
- Root cause: falha de integração entre sistemas
- User impact: bloqueios repetidos
- Operational impact: retrabalho e perda de eficiência

## Conclusão
A falha do serviço não aparece apenas no momento do bloqueio. Ela se manifesta em todo o ecossistema: comunicação, operação, suporte e infraestrutura.

## Oportunidade
Ao mapear falhas dessa forma, o projeto consegue priorizar melhorias que reduzem fricção sem abrir brechas para fraude.
