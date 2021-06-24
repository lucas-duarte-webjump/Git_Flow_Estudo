# GIT FLOW

## Como funciona?

O git flow trabalho com dois fluxos de ramificações para registrar o histórico do projeto. A branch `principal` armazena o histórico do lançamento oficial e a ramificação de `desenvolvimento` serve como uma ramificação de integração para recursos. Também é conveniente marcar todos os commits no branch principal com o numero de versão.

## Passos

- Na branch `principal`  master/main vamos complementar com uma ramificação/branch de desenvolvimento.
    - No seu projeto que já foi feito `git init`  e postado alguma pasta em seu repositório remoto, crie uma branch develop `git branch develop` , após faça um push desta branch para o repositório remoto.
    - A branch develop irá conter o histórico completo do projeto, enquanto a branch master/main irá conter uma versão abreviada.
    - Execute o `git flow init` no repositório existente vai criar uma ramificação de desenvolvimento