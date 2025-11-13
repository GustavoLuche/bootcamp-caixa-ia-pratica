# Guia de Uso do GitHub Copilot no Bootcamp CAIXA IA

> Este guia ajuda a potencializar o aprendizado integrando IA no seu fluxo diário.

## 1. Estratégia Geral de Uso

| Fase | Objetivo | Ação com Copilot |
|------|----------|------------------|
| Planejamento | Definir escopo e arquitetura | "@workspace Sugira estrutura para [projeto] com foco em [objetivo]" |
| Implementação | Gerar código inicial | Especificar claramente requisitos e linguagem |
| Refatoração | Melhorar qualidade | Copilot Chat: "/review" + critérios (performance, legibilidade) |
| Testes | Garantir funcionamento | Selecionar função → "/tests" e ajustar casos |
| Documentação | Facilitar entendimento | Selecionar bloco → "/doc" |
| Aprendizado | Fixar conceitos | Perguntas teóricas + exemplos práticos |
| Revisão contínua | Evolução incremental | Perguntar "Quais próximos passos de melhoria?" |

## 2. Prompt Engineering (Exemplos Práticos)

Use formato estruturado:
```
Contexto: Estou desenvolvendo um organizador financeiro com IA que classifica gastos automaticamente.
Objetivo: Criar função para categorizar transações usando palavras-chave e fallback por modelo simples.
Restrições: Código em Python, sem dependências pesadas, pronto para teste unitário.
Saída esperada: Função + exemplo de uso + sugestão de testes.
```

Melhorando prompts:
- Especifique linguagem, restrições e formato de saída.
- Indique o estágio (rascunho, otimização, testes).
- Peça explicação quando o foco for aprendizado: "Explique cada passo brevemente".

### Templates Úteis
```
@workspace Preciso criar [feature]. Dados disponíveis: [lista]. Regras: [lista]. Gere: [itens].
```
```
Explique diferença entre [conceito 1] e [conceito 2] com analogia simples e exemplo em código.
```
```
Refatore este código para: 1) diminuir complexidade ciclomática, 2) extrair constantes, 3) adicionar tratamento de erros.
```

## 3. Fluxo Diário Sugerido

Manhã:
1. Revisar lista de tarefas → Perguntar: "Sugira divisão de etapas para [tarefa maior]".
2. Planejar arquitetura/estrutura.
3. Gerar rascunho inicial do código.

Tarde:
4. Rodar refatorações específicas.
5. Criar testes automatizados.
6. Documentar principais funções.
7. Registrar aprendizados em `anotacoes/`.

## 4. Boas Práticas de Código com Copilot
- Sempre revise código sugerido (erros lógicos podem ocorrer).
- Valide entradas (não confie em suposições do modelo).
- Mantenha funções curtas e coesas para melhorar sugestões.
- Solicite alternativas: "Me dê 2 abordagens diferentes".
- Para otimização: "Explique trade-offs desta solução".

## 5. Revisão e Qualidade
Checklist para "/review":
- Nome de variáveis significativo?
- Tratamento de erros adequado?
- Comentários só onde agregam?
- Funções <= ~30 linhas?
- Complexidade aceitável?
- Testes cobrindo casos principais e de erro?

## 6. Testes com Copilot
Prompt para gerar testes:
```
Gere testes unitários para a função X cobrindo:
- Caso base
- Entrada inválida
- Limites
- Caso de exceção
Formato: pytest
```

## 7. Aprendizado Acelerado
Transforme respostas em resumos:
```
Resuma em 5 bullets principais pontos sobre [tema].
```

Crie mini flashcards:
```
Liste 8 perguntas e respostas rápidas sobre [assunto].
```

## 8. Mentorias
Antes da live:
- Levantar dúvidas: "Liste perguntas inteligentes sobre [tema]".
Após a live:
- Resumir: "Estruture os pontos principais discutidos sobre [tópico]".

## 9. Evitando Armadilhas
| Risco | Mitigação |
|-------|-----------|
| Aceitar código sem entender | Solicitar explicação passo a passo |
| Prompt vago | Usar estrutura Contexto/Objetivo/Restrições/Saída |
| Dependências desnecessárias | Pedir versão sem libs externas |
| Falta de testes | Gerar testes antes de refatorar |
| Perder aprendizado | Registrar em `anotacoes/` imediatamente |

## 10. Integração com o Repositório
- Criar branches por feature: `feature/organizador-categorizacao`.
- Pedir sugestões de nome de branch: "Sugira 3 nomes sem espaços para esta feature".
- Gerar mensagens de commit: "Sugira commit convencional para: [descrição]".

## 11. Formatos de Saída Desejáveis
Peça explicitamente:
- "Código + explicação breve"
- "Somente lista de passos, sem código"
- "Tabela comparativa entre [x] e [y]"

## 12. Evolução Contínua
Perguntas semanais:
- "Quais melhorias posso aplicar ao projeto X?"
- "Quais lacunas de aprendizado tenho considerando meus arquivos?"

## 13. Atalhos de Uso (Resumo Rápido)
- Planejar: "Estruture [projeto]"
- Implementar: "Gerar função [nome] com [regras]"
- Refatorar: "/review" + critérios
- Testar: "/tests" em seleção
- Documentar: "/doc"
- Aprender: "Explique [conceito] e compare com [conceito]"

---

Mantenha este arquivo vivo: adicione novos prompts eficazes e lições aprendidas.
