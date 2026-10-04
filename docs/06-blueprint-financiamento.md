# 06. Blueprint visual do serviço: financiamento de veículo no app bancário

## Contexto do cenário
Um cliente do banco acessa o app para financiar a compra de um veículo. O objetivo é facilitar a simulação, a análise de crédito e a contratação, sem gerar fricção desnecessária e sem comprometer os controles de risco.

## Blueprint visual

```mermaid
flowchart TB
    subgraph USER[Usuário / Cliente]
        U1[Abre o app]
        U2[Busca financiamento para veículo]
        U3[Consulta simulação]
        U4[Escolhe veículo e valor]
        U5[Envia documentos]
        U6[Recebe análise de crédito]
        U7[Confirma contrato]
        U8[Recebe liberação do crédito]
    end

    subgraph FRONT[FRONTSTAGE / O que o usuário vê]
        F1[Home do app]
        F2[Ofertas de financiamento]
        F3[Simulador de crédito]
        F4[Checklist de documentos]
        F5[Status da análise]
        F6[Mensagem de aprovação / pendência]
        F7[Resumo do contrato]
        F8[Assinatura digital]
    end

    subgraph BACK[BACKSTAGE / Operação]
        B1[Atendimento digital]
        B2[Analista de crédito]
        B3[Validação documental]
        B4[Validação do veículo]
        B5[Operações de risco]
        B6[Comercial / relacionamento]
        B7[Gestão de pendências]
    end

    subgraph DECISION[DECISION LAYER]
        D1[Sinais de risco]
        D2[Score de crédito]
        D3[Regra de política do banco]
        D4[Decisão: aprovar / revisar / negar]
    end

    subgraph DATA[DATA]
        DA1[Dados cadastrais]
        DA2[Receita e comprovantes]
        DA3[Histórico bancário]
        DA4[Valor do veículo]
        DA5[Perfil de risco]
        DA6[Documentos enviados]
    end

    subgraph TECH[TECHNICAL BACKSTAGE]
        T1[App bancário]
        T2[API de simulação]
        T3[Fraud engine]
        T4[Credit scoring]
        T5[Document validation]
        T6[Core banking]
        T7[CRM / atendimento]
        T8[Logs e auditoria]
    end

    U1 --> F1
    F1 --> U2
    U2 --> F2
    F2 --> U3
    U3 --> F3
    F3 --> U4
    U4 --> F4
    F4 --> U5
    U5 --> F5
    F5 --> U6
    U6 --> F6
    F6 --> U7
    U7 --> F7
    F7 --> U8
    F8 --> F8

    F2 --> B1
    F3 --> B1
    F4 --> B3
    F5 --> B2
    F6 --> B5
    F7 --> B6
    F7 --> B7

    B2 --> D1
    B3 --> D1
    B4 --> D1
    D1 --> D2
    D2 --> D3
    D3 --> D4
    D4 --> F6

    DA1 --> D2
    DA2 --> D2
    DA3 --> D2
    DA4 --> D2
    DA5 --> D3
    DA6 --> D3

    T1 --> F1
    T2 --> F3
    T3 --> D1
    T4 --> D2
    T5 --> B3
    T6 --> F8
    T7 --> B1
    T8 --> B5
```

## Interpretação do blueprint

### Camada de usuário
O cliente interage diretamente com o app para:

- encontrar a melhor opção de financiamento;
- simular parcelas;
- escolher veículo;
- enviar documentação;
- acompanhar status da análise;
- assinar contrato.

### Camada de interface / frontstage
O app precisa ser claro, rápido e confiável. Ele transmite:

- proposta de crédito;
- explicação do processo;
- documentação necessária;
- status atualizado da análise;
- mensagens de aprovação, pendência ou negativa.

### Camada de operação / backstage
Por trás do app, o banco precisa executar:

- atendimento digital;
- análise de crédito;
- validação documental;
- validação do veículo;
- revisão do risco;
- gestão de pendências.

### Camada de decisão
A decisão do banco depende de:

- sinais de risco;
- score de crédito;
- políticas internas;
- histórico do cliente;
- valor e perfil do veículo.

### Camada de dados
O processo precisa integrar:

- dados cadastrais;
- receitas e comprovantes;
- histórico bancário;
- valor do veículo;
- documentos enviados;
- nível de risco do cliente.

### Camada técnica
Os sistemas podem incluir:

- app bancário;
- API de simulação;
- fraud engine;
- credit scoring;
- validadores de documento;
- core banking;
- CRM;
- logs e auditoria.

## Pontos de fricção esperados
- necessidade de enviar muitos documentos;
- dúvida sobre o motivo da pendência;
- demora na análise;
- comunicação genérica sobre aprovação ou recusa;
- falta de clareza sobre o status do contrato.

## Oportunidades de melhoria de serviço
- explicar melhor o motivo da solicitação documental;
- reduzir etapas repetitivas;
- oferecer status claro e progressivo;
- mostrar qual parte do processo está em análise;
- permitir revisão de pendências sem perder contexto;
- adaptar a fricção ao nível de risco do cliente;
- assegurar que o usuário entenda a decisão sem se sentir rejeitado.

## Conclusão
Esse blueprint mostra que, em um app de banco para financiamento de veículo, o problema não está somente em aprovar ou negar o crédito. O verdadeiro desafio está em conectar a experiência do cliente, a operação do banco, as regras de risco e os sistemas técnicos em uma jornada coerente, compreensível e confiável.
