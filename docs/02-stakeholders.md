# 02. Stakeholders e atores do serviço

## Visão geral
O serviço de prevenção a fraude não é composto apenas por usuários e regras. Ele envolve múltiplos atores com diferentes objetivos e necessidades.

## Atores principais

### 1. Usuário legítimo
- quer concluir sua operação rápida e com segurança;
- não quer passar por fricção desnecessária;
- precisa entender o motivo de uma verificação ou bloqueio;
- valoriza transparência e controle.

### 2. Fraudster / malicious actor
- tenta explorar vulnerabilidades;
- busca burlar regras, autenticação e validações;
- aumenta o risco para a operação e para o negócio.

### 3. Fraud / Risk Analyst
- avalia sinais, casos e regras acionadas;
- decide quando a operação precisa ser revisada ou bloqueada;
- depende de contexto e dados para tomar decisões consistentes.

### 4. Customer Support Agent
- atende usuários impactados;
- precisa explicar a decisão de risco com clareza;
- frequentemente atua como elo entre experiência e operação.

### 5. Product / Risk Team
- define estratégias de prevenção;
- ajusta regras, políticas e critérios de decisão;
- busca equilibrar proteção, conversão e eficiência operacional.

### 6. Canais digitais
- app, web, notificação, suporte, comunicação, jornada de onboarding;
- funcionam como camada de interação entre o usuário e o backend.

### 7. Sistemas e plataformas internas
- identity provider;
- fraud engine;
- payment infrastructure;
- CRM;
- case management;
- logs e bancos de dados.

## Interesses e conflitos
| Ator | Principal interesse | Potencial conflito |
|---|---|---|
| Usuário legítimo | segurança com pouca fricção | bloqueios e falta de clareza |
| Fraudster | explorar brechas | medidas de proteção |
| Risk Analyst | reduzir perdas e riscos | falsos positivos |
| Support Agent | resolver casos rapidamente | falta de contexto |
| Product / Risk | conversão + proteção | regras excessivas |
| Sistemas | automatizar decisões | contexto incompleto |

## Conclusão
O design do serviço precisa responder às necessidades de todos esses atores ao mesmo tempo. O foco não é apenas impedir fraude, mas também criar uma experiência coerente, compreensível e eficaz para os usuários legítimos.
