# Sistema de Almoxarifado e Central de Suporte

Aplicação web para controle de estoque, rastreabilidade de movimentações, planejamento de consumo, relatórios financeiros e atendimento de chamados internos.

> Status atual: planejamento concluído — [Sprint 0](https://github.com/GabrielPioDEV/sistema-almoxarifado/issues/1) aberta.

## Objetivos

O sistema deverá responder com segurança:

- quais produtos estão disponíveis e em qual quantidade;
- quem realizou cada entrada, retirada, ajuste ou estorno;
- quanto foi comprado e gasto em cada período;
- quais itens precisam de reposição;
- se o consumo está dentro do planejamento mensal;
- como os chamados internos foram atendidos.

## Princípios do domínio

- Toda alteração de saldo gera uma movimentação identificável.
- Movimentações confirmadas não são apagadas; correções usam estorno.
- O preço pertence à entrada de estoque, não ao produto.
- Retiradas nunca podem deixar o estoque negativo.
- Regras críticas são validadas no backend e, quando aplicável, no banco.
- O acesso é negado por padrão e liberado conforme o papel do usuário.

## Arquitetura e tecnologias

O projeto será desenvolvido como um **monólito modular**, mantendo a implantação simples e separando claramente os módulos de catálogo, estoque, planejamento, relatórios, administração e suporte.

| Camada | Tecnologia planejada |
| --- | --- |
| Backend e páginas web | Ruby 3.4.x, Rails 8.1, ERB e Hotwire |
| Banco de dados | PostgreSQL 18 |
| Autenticação | Gerador nativo do Rails |
| Autorização | Pundit |
| Arquivos e fotos | Active Storage |
| Testes | Minitest e Capybara |
| Qualidade e segurança | RuboCop, Brakeman e bundler-audit |
| Ambiente | Docker e Docker Compose |
| Integração contínua | GitHub Actions |

## Perfis iniciais

- **Requerente:** consulta itens, acompanha suas retiradas e abre chamados.
- **Almoxarifado:** gerencia catálogo, movimentações, planejamento e relatórios.
- **Suporte:** atende, transfere e encerra chamados.
- **Administrador:** gerencia usuários, configurações, permissões e auditoria.

## Roadmap

| Sprint | Entrega principal | Estado |
| --- | --- | --- |
| [0](https://github.com/GabrielPioDEV/sistema-almoxarifado/issues/1) | Ambiente, Git, Docker, PostgreSQL e CI | A iniciar |
| [1](https://github.com/GabrielPioDEV/sistema-almoxarifado/issues/2) | Produtos e categorias | Backlog |
| [2](https://github.com/GabrielPioDEV/sistema-almoxarifado/issues/3) | Autenticação e autorização | Backlog |
| [3](https://github.com/GabrielPioDEV/sistema-almoxarifado/issues/4) | Entradas de estoque e preços | Backlog |
| [4](https://github.com/GabrielPioDEV/sistema-almoxarifado/issues/5) | Retiradas, motivos e concorrência | Backlog |
| [5](https://github.com/GabrielPioDEV/sistema-almoxarifado/issues/6) | Histórico, ajustes, estornos e auditoria | Backlog |
| [6](https://github.com/GabrielPioDEV/sistema-almoxarifado/issues/7) | Estoque mínimo e dashboard | Backlog |
| [7](https://github.com/GabrielPioDEV/sistema-almoxarifado/issues/8) | Planejamento e relatórios mensais | Backlog |
| [8](https://github.com/GabrielPioDEV/sistema-almoxarifado/issues/9) | Permissões e administração | Backlog |
| [9](https://github.com/GabrielPioDEV/sistema-almoxarifado/issues/10) | Suporte do requerente | Backlog |
| [10](https://github.com/GabrielPioDEV/sistema-almoxarifado/issues/11) | Fila e painel do suporte | Backlog |
| [11](https://github.com/GabrielPioDEV/sistema-almoxarifado/issues/12) | Qualidade, segurança e desempenho | Backlog |
| [12](https://github.com/GabrielPioDEV/sistema-almoxarifado/issues/13) | Deploy e apresentação | Backlog |

As issues detalham a entrega, o estudo necessário e o critério de conclusão de cada sprint. Consulte também o [roadmap geral](https://github.com/GabrielPioDEV/sistema-almoxarifado/issues/14).

## Documentação

- [Especificação técnica completa](docs/ESPECIFICACAO_TECNICA.md)
- [Como contribuir](CONTRIBUTING.md)

## Estratégia de desenvolvimento

1. Selecionar uma issue da sprint atual.
2. Criar uma branch a partir de `main`.
3. Implementar e testar uma mudança pequena.
4. Abrir um pull request vinculado à issue.
5. Obter revisão e manter a integração contínua verde.
6. Fazer squash merge após cumprir a Definition of Done.

## Executando o projeto

Os comandos de instalação serão adicionados na Sprint 0, assim que a aplicação Rails e o Docker Compose forem criados. Ao final dessa sprint, qualquer integrante deverá conseguir iniciar aplicação e banco seguindo somente este README.

## Licença

A licença será definida pelo time antes da primeira versão pública utilizável.
