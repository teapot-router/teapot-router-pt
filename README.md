# Teapot Router

**Gateway de modelos de IA para desenvolvedores** — uma única chave para Claude Code e o SDK OpenAI em um único endpoint.

Site oficial: <https://teapotrouter.com/pt>

## - **Protocolo duplo**: Anthropic Messages (compatível com Claude Code) e OpenAI Chat Completions (`/v1`) com a mesma chave
- **Pagamento por uso e preços públicos**, com API JSON gratuita (`/api/pricing`)
- **Registro de custos por requisição**: modelo, tokens e valor a cada chamada
- **Chaves de organização e log de auditoria**
- **Failover automático multi-upstream**

## Início rápido (Claude Code)

```bash
export ANTHROPIC_BASE_URL=https://api.teapotrouter.com
export ANTHROPIC_AUTH_TOKEN=sk-xxxx
claude
```

## Início rápido (OpenAI SDK / Codex CLI)

```bash
export OPENAI_BASE_URL=https://api.teapotrouter.com/v1
export OPENAI_API_KEY=sk-xxxx
```

## Preços

Pagamento por uso (pré-pago a partir de US$ 1).
Preços: <https://teapotrouter.com/pt> / JSON: <https://teapotrouter.com/api/pricing>

## Sobre o projeto

- Projeto de desenvolvedor independente
- O nome vem do código HTTP 418 "I'm a teapot" 🫖
- Contato: support@teapotrouter.com