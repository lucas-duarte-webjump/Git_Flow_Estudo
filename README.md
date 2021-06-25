# GIT FLOW

## Como funciona?

O git flow trabalho com dois fluxos de ramificações para registrar o histórico do projeto. A branch `principal` armazena o histórico do lançamento oficial e a ramificação de `desenvolvimento` serve como uma ramificação de integração para recursos. Também é conveniente marcar todos os commits no branch principal com o numero de versão.

## Passos

- Na branch `principal` master/main vamos complementar com uma ramificação/branch de desenvolvimento.
  - No seu projeto que já foi feito `git init` e postado alguma pasta em seu repositório remoto, crie uma branch develop `git branch develop` , após faça um push desta branch para o repositório remoto.
  - A branch develop irá conter o histórico completo do projeto, enquanto a branch master/main irá conter uma versão abreviada.
  - Execute o `git flow init` no repositório existente vai criar uma ramificação de desenvolvimento

## Ramificação de recursos

- Novos recursos devem residir na própria ramificação, na qual pode ser enviada por push para o repositório central para backup. || Parte difícil de entender
- Os novos `recursos/feature` do sistemas serão ramificadas da branch de `desenvolvimento`, quando esse `recurso/feature` é finalizada, podemos unir ela ao seu pai, que é a branch de `desenvolvimento`

![Example](https://wac-cdn.atlassian.com/dam/jcr:8f00f1a4-ef2d-498a-a2c6-8020bb97902f/03%20Release%20branches.svg?cdnVersion=1675)

---

## Criando ramificações de recursos | Branch Feature

Com o git flow, é mais fácil criar uma branch de release

```bash
git flow feature start feature_branch
```

Ao finalizar sua feature podemos fazer o junção/merge com a branch de `desenvolvimento`

```bash
git flow feature finish feature_branch
```

A branch feature serve para criação de pacotes, de pequenas funcionalidades que serão adicionadas ao sistema, ela se bifurca da branch devolop. Após a finalização de tal funcionalidade, mesclamos a mesma com a branch de develop, trazendo assim esse pacote para nosso desenvolvimento

---

## Ramificações de lançamento

Quando a branch de desenvolvimento adquiriu recursos o bastante para um lançamento ou está preste do lançamento, pode-se bifurcar uma branch de `lançamento` a partir do `desenvolvimento.`

Criar esta ramificação dá início ao próximo ciclo de lançamento, portanto nenhum novo recurso pode ser adicionado depois deste ponto.

Quando a branch de `lançamento` está pronta ela é mesclada com a branch `principal/maser` assim marcando a branch principal/master com um numero de versão, esta branch deve-se mesclar com a branch de desenvolvimento também, para que possa prosseguir com novas funcionalidade para possíveis `lançamentos` futuros.

Para criarmos uma branch de `lançamento/release` no git flow, usamos o seguinte comando

```bash
git flow release start 0.1.0
```

O processo de mesclar de volta com a branch de `desenvolvimento` é importante porque atualizações importantes podem ter sido `adicionadas` à branch de `lançamento` e elas devem ser acessíveis a novos recursos. Se sua organização enfatiza a revisão de códigos, este seria o local ideal para uma solicitação pull.

Para finalizar a branch de `lançamento`, usamos o seguinte comando:

```bash
git flow release finish '0.1.0'
```

**Como funciona a branch release**

![Example](https://wac-cdn.atlassian.com/dam/jcr:8f00f1a4-ef2d-498a-a2c6-8020bb97902f/03%20Release%20branches.svg?cdnVersion=1678)
