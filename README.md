# DocForge

> Um compilador de documentação para repositórios: lê o projeto, entende as instruções do desenvolvedor e transforma código e Markdown em documentação completa e navegável.

## O que é

DocForge é uma ferramenta CLI, open-source, que transforma um repositório de código em um site de documentação estático — navegável, com busca, temas claro/escuro e diagramas.

Diferente de gerar documentação "pedindo pra uma IA escrever", o DocForge propõe uma camada de engenharia entre o repositório e a IA:

```
Código + conhecimento existente + instruções do desenvolvedor → documentação estruturada
```

O desenvolvedor define o que deve ser documentado através de um arquivo `DOCS.md` na raiz do projeto. O DocForge usa essas instruções, os arquivos `.md` espalhados pelo repositório, a estrutura de pastas e, opcionalmente, o próprio código-fonte para construir a documentação.

## Status

🚧 **Em desenvolvimento inicial.** Projeto pessoal/playground, sem cronograma fixo.

## Como funciona (visão geral)

```
Repository
    │
    ▼
Scanner (markdown, source, estrutura, OpenAPI, git metadata)
    │
    ▼
Context Builder
    │
    ▼
Documentation Engine (geração determinística + IA opcional)
    │
    ▼
Documentation Renderer
    │
    ▼
Static Documentation
```

Um exemplo de `DOCS.md`:

```markdown
# Documentation Instructions

## Architecture
- Explain the project architecture
- Identify the main layers
- Generate an architecture diagram

## Modules
- Scan src/modules
- Use README.md files as additional context
- Document the responsibility of each module

## API
- Read the OpenAPI specification
- Document available endpoints

## Output
- Generate a searchable static website
```

## Roadmap

- **v1** — CLI + scanner determinístico + parser do `DOCS.md` + renderer estático (navegação, busca, tema claro/escuro)
- **v2** — `docforge dev` com hot reload, diagramas automáticos, cross-references, suporte a OpenAPI
- **v3** — camada de IA opcional (via integração com agente / MCP, com Ollama como opção local)

## Stack

Escrito em [Rust](https://www.rust-lang.org/).

## Uso planejado

```bash
npx docforge init   # cria as configurações iniciais
npx docforge build  # analisa o repositório e gera a documentação
npx docforge dev    # servidor local com atualização automática
```

## Licença

[MIT](LICENSE)
