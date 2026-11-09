# AXEV Config

Repositório de configuração remota do AXEV 3D Studio.

## Estrutura

```
config/
  workflow-config.json   — versões e metadados dos workflows
  workflow-options.json  — opções dos menus da app (Fase 2)
  flags.json             — feature flags (Fase 3)
workflows/
  ara-axev-crime.yml     — workflow de geração de personagem
  axev-smoke-test.yml    — workflow de smoke test
```

## Como funciona

A app Android busca este repositório antes de cada geração.
Se conseguir, usa a versão remota. Se falhar, usa a versão embutida no APK.

Para atualizar um workflow: edita o ficheiro em `workflows/` e incrementa a versão em `workflow-config.json`.
