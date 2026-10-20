---
title: "Lição 12 - Publique o site com o GitHub Pages"
description: "Use o app GitHub Copilot para configurar um workflow do Pages, revisar o pull request e confirmar que o Space Quiz está no ar."
authors:
  - jamesmontemagno
lastUpdated: 2026-10-12
---

Publique o Space Quiz no GitHub Pages para que qualquer pessoa possa acessar o site. O Copilot pode preparar o workflow e orientar a implantação, mas você é responsável por revisar as alterações e confirmar que o site está no ar.

Nesta lição, você vai:

- pedir ao Copilot para configurar a implantação no GitHub Pages.
- revisar o workflow e o pull request antes de fazer o merge.
- acompanhar a implantação e verificar o site publicado.

## Cenário

O Space Quiz já está em um repositório do GitHub, mas ainda falta uma maneira simples para as pessoas experimentarem o jogo. Publicar o site de arquivo único com o GitHub Pages o torna acessível por uma URL pública, sem adicionar um servidor ou uma dependência de runtime.

## Peça ao Copilot para publicar o site

Na sessão do app Copilot para `space-quiz`, envie este prompt:

```plaintext
Habilite o GitHub Pages para este repositório. Crie um workflow do GitHub Actions que compile o site, se necessário, e o implante no GitHub Pages. Se ainda não existir um README, adicione um que descreva o app e como executá-lo localmente. Crie um pull request com essas alterações e faça o merge depois que as verificações obrigatórias forem aprovadas. Acompanhe a implantação até ela ser concluída e informe a URL final do site no ar. Se você não tiver permissão para habilitar o Pages ou fazer o merge, diga exatamente o que preciso aprovar ou fazer; não informe que a tarefa foi concluída até o site estar no ar.
```

![Diagrama em três etapas: um pull request de space-quiz mesclado; uma execução bem-sucedida de Deploy website do GitHub Actions com as etapas Build website, Upload artifact e Deploy to Pages; e o Space Quiz publicado em yourname.github.io/space-quiz/.](../../../_images/first-steps-app-pages-deploy.svg)

> [!WARNING]
> Este prompt pede ao agente que crie e faça merge de um pull request e altere as configurações do Pages no repositório. Revise o diff, as permissões de implantação e eventuais solicitações de aprovação do GitHub antes de continuar.

## Revise o workflow e confirme a implantação

1. Confirme que o README foi adicionado somente se o repositório ainda não tiver um.
2. Revise as alterações do pull request, incluindo as etapas de build e implantação do workflow.
3. Faça merge somente depois que as verificações obrigatórias do pull request forem aprovadas.
4. Acompanhe a execução de implantação do GitHub Actions até ela ser concluída com sucesso.
5. Abra a URL informada e confirme que o Space Quiz carrega.

Se o agente não puder habilitar o Pages ou fazer merge do pull request, siga as instruções específicas fornecidas. Não considere a tarefa concluída até que a implantação tenha sucesso e o site esteja no ar.

## Resumo e próximos passos

O Space Quiz agora está disponível como um site, e você verificou a implantação em vez de confiar apenas no relato do agente. Continue para a [lição 13: Revisão e próximos passos][next-lesson].

[next-lesson]: ../13-review/
