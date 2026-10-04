# Designing Trust
## Service Design for Risk & Fraud

<p align="center">
  <img src="https://img.shields.io/badge/Service%20Design-Portfolio%20Case-orange" alt="Service Design portfolio case" />
  <img src="https://img.shields.io/badge/UX%20Research-User%20Insights-blue" alt="UX research" />
  <img src="https://img.shields.io/badge/Banking%20App-Financing%20Flow-green" alt="Banking app financing flow" />
  <img src="https://img.shields.io/badge/Focus-Risk%20%26%20Trust-purple" alt="Risk and trust" />
</p>

> Projeto fictício inspirado em experiências reais no setor financeiro, com foco em como reduzir fricção desnecessária em fluxos de financiamento digital sem comprometer a segurança.

### Pergunta central
Como tornar um serviço digital mais seguro sem criar fricção desnecessária para usuários legítimos?

---

## 🧭 Visão geral
Este projeto explora o equilíbrio entre:

- segurança e prevenção a fraude;
- experiência do cliente;
- eficiência operacional;
- confiança institucional.

A proposta parte de um cenário realista de um app bancário para financiamento de veículo, em que a decisão de risco impacta diretamente a jornada do cliente.

## 🎯 Objetivo do projeto
Compreender e propor melhorias para o fluxo de financiamento do cliente no app, reduzindo atrito, melhorando clareza e reforçando a confiança sem enfraquecer os controles de risco.

## 🧩 O que está dentro deste repositório

- [docs/01-briefing.md](docs/01-briefing.md) — briefing e contexto do projeto
- [docs/02-stakeholders.md](docs/02-stakeholders.md) — atores e stakeholders
- [docs/03-journey.md](docs/03-journey.md) — jornada do usuário
- [docs/04-service-blueprint.md](docs/04-service-blueprint.md) — blueprint do serviço
- [docs/05-failure-map.md](docs/05-failure-map.md) — falhas e impactos
- [docs/06-blueprint-financiamento.md](docs/06-blueprint-financiamento.md) — cenário visual de financiamento
- [docs/07-ux-research.md](docs/07-ux-research.md) — roteiro de entrevistas
- [docs/08-hipoteses-redesign.md](docs/08-hipoteses-redesign.md) — ideias de redesign
- [docs/09-metricas-sucesso.md](docs/09-metricas-sucesso.md) — indicadores de sucesso
- [docs/10-proposta-de-redesign.md](docs/10-proposta-de-redesign.md) — proposta do serviço redesenhado
- [docs/11-case-study-portfolio.md](docs/11-case-study-portfolio.md) — versão final para portfolio
- [presentation/README.md](presentation/README.md) — material visual para apresentação

---

## 1. Contexto
Serviços financeiros digitais precisam equilibrar duas exigências que costumam entrar em tensão:

- proteger a plataforma contra fraude;
- oferecer uma experiência simples e confiável para usuários legítimos.

Controles adicionais podem reduzir riscos, mas também aumentam fricção, geram falsos positivos e exigem mais esforço operacional. O projeto analisa o serviço como um ecossistema composto por usuários, canais, operações, regras de decisão, dados e sistemas.

---

## 2. Desafio
Cenário conceitual:

Uma fintech observa aumento de fricção durante uma jornada crítica. Usuários legítimos passam a receber verificações adicionais ou até ter operações bloqueadas por mecanismos de prevenção a fraude.

Esse cenário impacta diretamente:

- Usuário: frustração, insegurança, abandono;
- Negócio: queda em conversão e aprovação;
- Operação: aumento de contatos e análises manuais;
- Risk: necessidade de manter níveis adequados de proteção.

O problema central é a relação entre:

Fraud Prevention × Customer Experience × Operational Efficiency

---

## 3. Pesquisa e fundamentos
### Conceitos-chave
O projeto considera temas como:

- tipos comuns de fraude;
- identity fraud;
- account takeover;
- onboarding fraud;
- false positives;
- KYC;
- autenticação;
- biometria;
- mecanismos de recuperação;
- boas práticas de comunicação;
- impacto da fricção;
- prevenção a fraude versus conversão.

A investigação parte da ideia de que a segurança não deve ser vista apenas como uma camada técnica, mas como parte da experiência de serviço.

---

## 4. Personas e atores
Os principais atores e comportamentos relevantes para o serviço são:

### Usuário legítimo
Deseja concluir sua operação com segurança e o menor atrito possível.

### Fraudster / Malicious Actor
Tenta explorar vulnerabilidades do serviço para obter vantagem indevida.

### Fraud / Risk Analyst
Investiga casos e decisões sinalizadas pela plataforma.

### Customer Support Agent
Atende usuários afetados e precisa compreender o que aconteceu.

### Product / Risk Team
Define regras, políticas e melhorias do serviço.

Esse conjunto de atores reforça a lógica de um service design multi-actor.

---

## 5. Jornada atual
A jornada do usuário legítimo pode ser representada da seguinte forma:

Need
↓
Attempt
↓
Verification
↓
Risk evaluation
↓
Additional verification
↓
Blocked
↓
Confusion
↓
Support
↓
Manual review
↓
Resolution

---

## 6. Service Blueprint
A seguir, a estrutura do serviço em camadas.

### User journey
Attempt
↓
Verification
↓
Blocked
↓
Understand
↓
Contest
↓
Wait
↓
Resolution

### Line of interaction
- App
- Notification
- Verification
- Support
- Status
- Result

### Frontstage
- App
- Notificações
- Verificação
- Suporte
- Status da operação
- Resultado

### Backstage / Operations
- Customer Support
- Fraud Operations
- Manual Review
- Escalation
- Decision Review

### Decision layer
- Risk signals
- Rules
- Score
- Decision engine
- Approval / Review / Block

### Data
- Account
- Transaction
- Device
- Identity
- History
- Behavior
- Risk signals

### Technical backstage
- APIs
- Identity provider
- Fraud engine
- Payment infrastructure
- CRM
- Case management
- Logs
- Databases

---

## 7. Service Failure Map
Uma forma útil de analisar o problema é mapear falhas de serviço, causas, impactos para o usuário e impactos operacionais.

Exemplo:

- Legitimate user blocked → overly restrictive rule → frustration → support contact
- Generic error message → limited decision context → confusion → repeated contacts
- Support cannot explain → disconnected systems → distrust → escalation
- Manual review takes too long → fragmented process → abandonment → operational cost
- Reversal isn't propagated → integration failure → repeated block → rework

### Estrutura sugerida
Service Failure → Root Cause → User Impact → Operational Impact

---

## 8. Perspectiva de design
Abordei a prevenção de fraudes não apenas como um problema de segurança, mas como um desafio de design de serviços.

Uma decisão de risco tomada nos bastidores técnicos pode desencadear toda uma jornada do cliente, desde uma verificação adicional ou o bloqueio de uma transação até o atendimento ao cliente, a análise manual e a resolução do caso.

Ao conectar a experiência do cliente às operações, às regras de decisão, aos dados e aos sistemas, este projeto explora como o Design de Serviços pode ajudar a identificar onde os mecanismos de segurança geram atrito indesejado e onde o serviço pode oferecer melhor suporte a usuários legítimos, sem comprometer os controles de risco.

O objetivo não é eliminar o atrito por completo, mas torná-lo proporcional, compreensível e reversível.

Uma boa estratégia de prevenção a fraude deve barrar agentes maliciosos sem projetar cada jornada como se todo cliente fosse um potencial risco.

---

## 9. Conclusão
O projeto busca compreender como a segurança e a experiência do usuário podem coexistir de forma mais equilibrada. A principal ideia é que a prevenção a fraude deve ser projetada como um serviço, e não apenas como um conjunto de regras técnicas.

A partir dessa visão, é possível reduzir fricção desnecessária, melhorar a clareza das decisões e fortalecer a confiança do usuário no serviço.

---

## 10. Próximos passos sugeridos
- mapear jornadas por segmento de usuário;
- definir indicadores de fricção e falso positivo;
- identificar pontos de ruptura no serviço;
- propor melhorias de comunicação e experiência;
- testar hipóteses com foco em equilíbrio entre segurança e conversão.

---

## 11. Contexto profissional e origem do projeto
Este projeto está fundamentado em experiências profissionais que já desenvolvi em serviços financeiros e em ambientes de produto digital. Ele parte de situações reais observadas em jornadas de clientes, operação de risco e tomada de decisão de produto, em que o equilíbrio entre segurança, conversão e confiança do usuário se torna crítico.

O objetivo é transformar a experiência prática em uma abordagem estruturada de service design, usando pensamento de serviço para identificar onde a fricção é criada, como os usuários percebem as decisões de risco e como o banco pode melhorar a experiência de financiamento sem enfraquecer os controles contra fraude.

---

## 12. UX Research
### Objetivo
Entender os principais pontos de dificuldade vivenciados por usuários ao tentar financiar um veículo por meio de um app bancário e identificar oportunidades para melhorar a usabilidade, a clareza e a confiança no processo.

### Abordagem da pesquisa
Vamos realizar entrevistas qualitativas com usuários que já usaram ou tentaram usar o app para solicitar financiamento de veículo. O objetivo é compreender seu processo de decisão, reações emocionais, dúvidas e pontos de fricção durante a jornada.

### Participantes
- usuários que já solicitaram financiamento pelo app;
- usuários que iniciaram o fluxo, mas abandonaram;
- usuários que tiveram dificuldade para entender decisões ou documentos solicitados;
- usuários com diferentes perfis de familiaridade digital e histórico de crédito.

### Roteiro de entrevista
1. Pode me contar sobre sua experiência ao tentar financiar um veículo pelo app?
2. Qual foi a primeira coisa que você procurou no app?
3. Você entendeu os passos necessários para concluir a solicitação de financiamento?
4. Houve algum momento em que você se sentiu confuso ou inseguro?
5. Quais informações ou documentos você achou mais difíceis de entender ou encontrar?
6. Como você avaliou se a oferta de financiamento estava clara e confiável?
7. O app explicou por que foi solicitada uma verificação adicional ou mais documentos?
8. O que te deu mais confiança ou menos confiança durante o processo?
9. Houve momentos em que o processo pareceu longo, repetitivo ou complicado?
10. O que você mudaria para tornar o fluxo de financiamento mais simples e transparente?
11. O app ajudou você a entender os riscos, as condições e o fluxo de aprovação?
12. Na sua opinião, qual é a principal melhoria necessária para tornar esse processo mais usável?

### O que queremos identificar
- pontos de confusão no fluxo;
- tarefas que os usuários têm dificuldade para concluir;
- momentos de decisão pouco claros;
- fricção excessiva ou desnecessária;
- lacunas de comunicação entre a decisão do sistema e a compreensão do usuário;
- elementos que reduzem a confiança no processo digital;
- oportunidades para simplificar e esclarecer a oferta.

### Resultados esperados
- entendimento mais claro dos pontos de dor do usuário;
- definição de problemas de usabilidade prioritários;
- suporte para redesenhar a jornada de financiamento;
- melhor alinhamento entre políticas do banco, design de produto e experiência do cliente.

---

## 13. Próximo passo esperado
A próxima etapa é transformar este projeto conceitual em um artefato mais concreto de service design, combinando:

- mapeamento da jornada com base nas entrevistas;
- service blueprint do fluxo de financiamento;
- identificação de pontos de fricção e causas raiz;
- priorização de melhorias de design;
- validação com usuários e stakeholders internos.

Este é um projeto fictício, inspirado em minha jornada profissional e em experiências reais vividas no setor financeiro.

---

## Documentação do projeto

A estrutura completa do case está organizada em arquivos dedicados para facilitar leitura e apresentação em portfolio:

- [docs/00-indice.md](docs/00-indice.md)
- [docs/01-briefing.md](docs/01-briefing.md)
- [docs/02-stakeholders.md](docs/02-stakeholders.md)
- [docs/03-journey.md](docs/03-journey.md)
- [docs/04-service-blueprint.md](docs/04-service-blueprint.md)
- [docs/05-failure-map.md](docs/05-failure-map.md)
- [docs/06-blueprint-financiamento.md](docs/06-blueprint-financiamento.md)
- [docs/07-ux-research.md](docs/07-ux-research.md)
- [docs/08-hipoteses-redesign.md](docs/08-hipoteses-redesign.md)
- [docs/09-metricas-sucesso.md](docs/09-metricas-sucesso.md)
- [docs/10-proposta-de-redesign.md](docs/10-proposta-de-redesign.md)
- [docs/11-case-study-portfolio.md](docs/11-case-study-portfolio.md)
