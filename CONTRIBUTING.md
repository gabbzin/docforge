# Contribuindo com o DocForge

Obrigado pelo interesse em contribuir! O projeto ainda está em fase inicial, então as regras abaixo são propositalmente enxutas.

## Antes de começar

- Abra uma **issue** antes de uma PR grande, pra alinhar escopo e evitar retrabalho.
- Para bugs simples, typos ou melhorias pequenas, pode ir direto pra PR.

## Ambiente de desenvolvimento

Pré-requisitos:

- [Rust](https://www.rust-lang.org/tools/install) (edição estável mais recente)
- `cargo`

```bash
git clone https://github.com/<seu-usuario>/docforge.git
cd docforge
cargo build
cargo test
```

## Padrões de código

- Rode `cargo fmt` antes de commitar.
- Rode `cargo clippy` e resolva os warnings antes de abrir a PR.
- Mantenha commits pequenos e com mensagens claras (preferencialmente no formato [Conventional Commits](https://www.conventionalcommits.org/): `feat:`, `fix:`, `docs:`, `chore:`, etc.).

## Pull Requests

1. Fork o repositório e crie uma branch a partir de `main`: `git checkout -b feat/minha-feature`.
2. Garanta que `cargo build`, `cargo test` e `cargo clippy` passam localmente.
3. Descreva na PR o que mudou e por quê.
4. Uma PR só é mergeada após revisão e aprovação.

## Código de conduta

Ao contribuir, você concorda em seguir o [Código de Conduta](CODE_OF_CONDUCT.md) do projeto.

## Dúvidas

Abra uma issue com a tag `question`.
