# Gemini 4 China access / usage summary

[中文](./README.md) · Original article (Chinese, CSDN): <https://blog.csdn.net/xianyu120/article/details/167808730>

How to use **Gemini 4** (`gemini-4-argon` / `gemini-4-barium`) from China — pricing, endpoints, and examples in one place. On 2026-10-13, [tryallapi](https://tryallapi.com/) announced these models. See also the [TryGPT model list](https://trygpt.asia/list/#/home). Descriptions below come from the tryallapi model marketplace only (no benchmarks run); check the site for specs such as context length.

- **gemini-4-argon** – site description: strong at coding, reasoning, multimodal and long-running multi-step tasks for enterprise workflows.
- **gemini-4-barium** – site description: "Gemini4 internal iteration candidate prototype (Barium-B evolved into Argon)", million-token context, multimodal, code / legal-finance / vulnerability reasoning, tool calling.
- Tags (both): chat / vision / tools. Vendor: Google.

## Pricing (as of 2026-10-13, see site for current)

| Model | Input | Output | Cache hit | Groups |
| --- | --- | --- | --- | --- |
| `gemini-4-argon` | $0.2941 / 1M | $1.4710 / 1M | $0.0147 / 1M | Anti-Gemini-1, Cli-Gemini-1 |
| `gemini-4-barium` | $0.2941 / 1M | $1.4710 / 1M | $0.0147 / 1M | Anti-Gemini-1, Cli-Gemini-1 |

## Usage

Endpoints: `POST /v1/chat/completions` (OpenAI) and `POST /v1beta/models/{model}:generateContent` (Gemini). Base URL: `https://tryallapi.com/v1`. Use a token in group Anti-Gemini-1 or Cli-Gemini-1.

```bash
curl https://tryallapi.com/v1/chat/completions \
  -H "Authorization: Bearer $TRYALLAPI_KEY" \
  -H "Content-Type: application/json" \
  -d '{"model": "gemini-4-argon", "messages": [{"role": "user", "content": "Explain RAG in three sentences"}]}'
```

Sign up: <https://tryallapi.com/register?aff=5A6A>

## Links

- tryallapi: <https://tryallapi.com/>
- TryGPT model list (API site): <https://trygpt.asia/list/#/home>
- TryGPT homepage: <https://trygpt.asia/>
