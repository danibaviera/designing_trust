# 04. Service Blueprint

## Objetivo
Representar o serviço em camadas para entender como as decisões de risco, a operação e a experiência do usuário se conectam.

## User journey
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

## 1. Line of interaction
- App
- Notification
- Verification
- Support
- Status
- Result

## 2. Frontstage
- app
- notificações
- verificação
- suporte
- status da operação
- resultado

## 3. Backstage / Operations
- Customer Support
- Fraud Operations
- Manual Review
- Escalation
- Decision Review

## 4. Decision layer
- Risk signals
- Rules
- Score
- Decision engine
- Approval / Review / Block

## 5. Data
- Account
- Transaction
- Device
- Identity
- History
- Behavior
- Risk signals

## 6. Technical backstage
- APIs
- Identity provider
- Fraud engine
- Payment infrastructure
- CRM
- Case management
- Logs
- Databases

## Observações
- a decisão de risco pode acontecer sem que o usuário veja o contexto completo;
- o suporte precisa entender a lógica da decisão para responder adequadamente;
- a experiência do usuário depende da comunicação, do tempo de resposta e da previsibilidade do processo.

## Conclusão
O blueprint mostra que a qualidade do serviço depende da coerência entre interface, operação, regra de decisão e infraestrutura técnica.
