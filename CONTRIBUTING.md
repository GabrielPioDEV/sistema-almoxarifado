# Como contribuir

## Fluxo de trabalho

1. Escolha uma issue da sprint atual e confirme que ela não está atribuída a outra pessoa.
2. Atualize a branch `main`.
3. Crie uma branch curta e relacionada à issue:
   - `feature/12-cadastro-produtos`
   - `fix/31-bloqueio-estoque-negativo`
   - `docs/4-atualiza-readme`
4. Faça commits pequenos usando Conventional Commits:
   - `feat: adiciona cadastro de categorias`
   - `fix: impede retirada acima do saldo`
   - `test: cobre estorno de movimentação`
   - `docs: documenta ambiente local`
5. Abra um pull request e use `Closes #NUMERO` na descrição.
6. Aguarde a revisão antes do merge.

## Definition of Done

Uma tarefa só é concluída quando:

- os critérios de aceite da issue foram atendidos;
- as regras estão validadas no backend;
- migrations possuem índices e constraints adequados;
- testes relevantes foram criados ou atualizados;
- lint, análise de segurança e testes passam;
- não existem segredos ou dados sensíveis versionados;
- a documentação foi atualizada quando necessário;
- o pull request foi revisado e integrado à `main`.

## Pull requests

Mantenha cada pull request focado em uma única issue. Inclua:

- o problema resolvido;
- a solução adotada;
- como testar;
- capturas de tela para mudanças visuais;
- riscos, migrations ou decisões importantes;
- referência à issue relacionada.

## Revisão

Na revisão, verifique principalmente regras de negócio, autorização, transações, concorrência, integridade do banco, testes e clareza do código.
