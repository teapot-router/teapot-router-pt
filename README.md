<div align="center">

# Teapot Router — gateway de API LLM para agentes de código

**Uma chave. Dois protocolos. Pague pelo uso — e o saldo nunca expira.**

Gateway hospedado para Claude Code, Codex CLI e ferramentas com OpenAI SDK: troque duas variáveis de ambiente e todas as suas ferramentas de código com IA passam por um único endpoint, um único saldo, um livro de custos por requisição.

[Começar](https://teapotrouter.com/pt/register) · [Preços — públicos, JSON legível por máquina](https://teapotrouter.com/api/pricing) · [Documentação](https://teapotrouter.com/pt/docs)

</div>

---

## Por que um gateway para agentes de código?

Se você usa Claude Code junto de ferramentas do OpenAI SDK, já conhece o problema: cada ferramenta quer seu endpoint e sua chave, e a fatura vira uma caixa-preta mensal.

Um gateway organiza o encanamento:

| | Conexão direta (por fornecedor) | Via gateway |
| --- | --- | --- |
| Endpoints e chaves | um por fornecedor | **uma chave, dois protocolos** |
| Faturamento | N painéis, totais mensais | um saldo, **livro por requisição** |
| Visibilidade de custo | "foram $84" | "essa sessão custou $6.20 — 78% foi contexto reenviado" |
| Condições | política de cada fornecedor | aqui: **saldo sem validade**, reembolso pelo saldo restante |

## Configuração: duas variáveis de ambiente

```bash
# Claude Code (protocolo Anthropic)
export ANTHROPIC_BASE_URL="https://api.teapotrouter.com"
export ANTHROPIC_AUTH_TOKEN="sk-****"

# OpenAI SDK / Codex CLI — mesma chave, endpoint /v1
# base_url = https://api.teapotrouter.com/v1
```

Guias passo a passo (registro → primeira requisição → solução de problemas): [teapotrouter.com/pt/docs](https://teapotrouter.com/pt/docs)

## O que você encontra no site

- **Preços públicos** — tarifa base e preço realmente pago de cada modelo, com um endpoint JSON sem login ([`/api/pricing`](https://teapotrouter.com/api/pricing)) para comparar via script
- **Página de preços por modelo** — ex.: [claude-opus-5-5](https://teapotrouter.com/pt/pricing/claude-opus-5-5)
- **Guia de preços do Claude Code** — assinatura vs pagamento por uso vs gateway, com a conta real: [documentação](https://teapotrouter.com/pt/docs/claude-code-pricing)
- **Guia de solução de problemas** — conexão, 401 e erros de cota pareados com a correção: [documentação](https://teapotrouter.com/pt/docs/claude-code-troubleshooting)

## Duas perguntas para fazer a qualquer gateway (inclusive este)

- **De onde vêm os modelos?** De canais de API oficiais/autorizados, medidos e pagos por uso. Sem contas compartilhadas, sem revenda de assinaturas.
- **O que é registrado?** Apenas metadados de cobrança (modelo, tokens, custo, latência) — é o que torna o livro por requisição possível. Não fazemos teatro de "zero log"; não tocamos no conteúdo das conversas.

## Limites honestos

Projeto solo, lançado recentemente, sem verba de marketing — o endpoint de preços sempre mostra a lista viva de modelos: confira você mesmo em vez de confiar neste README. O failover multi-upstream é embutido, mas um gateway continua sendo uma dependência: mantenha um caminho alternativo.

Contato: support@teapotrouter.com

---

<div align="center">

O nome vem do código de status HTTP 418 "I'm a teapot" 🫖 — [a história completa](https://teapotrouter.com/pt/418)

**[Teapot Router](https://teapotrouter.com/pt)** — gateway de IA stability-first para Claude Code e GPT.

</div>
