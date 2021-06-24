# GIT FLOW

## Como funciona?

O git flow trabalho com dois fluxos de ramificações para registrar o histórico do projeto. A branch `principal` armazena o histórico do lançamento oficial e a ramificação de `desenvolvimento` serve como uma ramificação de integração para recursos. Também é conveniente marcar todos os commits no branch principal com o numero de versão.

## Passos

- Na branch `principal`  master/main vamos complementar com uma ramificação/branch de desenvolvimento.
    - No seu projeto que já foi feito `git init`  e postado alguma pasta em seu repositório remoto, crie uma branch develop `git branch develop` , após faça um push desta branch para o repositório remoto.
    - A branch develop irá conter o histórico completo do projeto, enquanto a branch master/main irá conter uma versão abreviada.
    - Execute o `git flow init` no repositório existente vai criar uma ramificação de desenvolvimento
## Ramificação de recursos

- Novos recursos devem residir na própria ramificação, na qual pode ser enviada por push para o repositório central para backup. || Parte difícil de entender
- Os novos `recursos/feature` do sistemas serão ramificadas da branch de `desenvolvimento`,   quando esse `recurso/feature` é finalizada, podemos unir ela ao seu pai, que é a branch de `desenvolvimento`

![Example](https://wac-cdn.atlassian.com/dam/jcr:8f00f1a4-ef2d-498a-a2c6-8020bb97902f/03%20Release%20branches.svg?cdnVersion=1675)
