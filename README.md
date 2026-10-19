# Crowns — protótipo acadêmico

Protótipo de jogo de cartas em JavaFX, com combate por turnos, três arenas e recompensas em memória. O repositório contém partes implementadas do jogo e estruturas ainda incompletas; não representa a versão com integração PostgreSQL disponível em [Crowns](https://github.com/Heitorsv001/Crowns).

## O que está implementado

- Menu com entrada do nome do jogador e início de uma sessão.
- Batalha por turnos, deck inicial com quatro cartas, vida, elixir e recarga.
- Cálculos de dano crítico e cura.
- Progressão por três arenas, recompensas em moedas e possibilidade de carta bônus.
- Tela de recompensa e exibição das estatísticas da sessão.

Esses recursos são identificados nos Models e Controllers. A interface completa não foi executada nesta revisão.

## Partes incompletas

- A loja apresenta o saldo, mas não implementa compras ou upgrades pela interface. Existem regras correspondentes no Model, sem integração da tela.
- `DeckController` está vazio e `deck.fxml` não possui conteúdo funcional para edição do deck.
- As classes DAO são estruturas vazias. Não há persistência, script SQL, conexão com banco ou driver JDBC declarado.
- O histórico mostra estatísticas da sessão, sem registro detalhado de partidas.
- `creditos.fxml` termina em uma tag incompleta e falhou na validação XML. A abertura dessa tela está comprometida.
- Iniciar outra sessão cria um novo jogador; o estado não é recuperado após fechar a aplicação.

## Tecnologias e organização

O [pom.xml](pom.xml) configura compilação Java 11, JavaFX Controls e FXML 13, Maven Compiler Plugin e JavaFX Maven Plugin. Essas são as versões declaradas, sem validação de compatibilidade em execução nesta revisão.

O código está separado em `model`, `controller`, `utils` e `com/mycompany/crowns/dao`. As telas ficam em `src/main/resources/com/mycompany/crowns/`, com FXML, CSS e imagens. A separação de Models, Controllers e Views FXML está presente, mas a camada de dados ainda não possui implementação.

## Preparação e tentativa de execução

Requisitos previstos pelo projeto: JDK compatível com o alvo Java 11 e com JavaFX 13, Maven, conexão para baixar dependências e ambiente gráfico. Não há banco de dados, `.env` ou configuração de serviços externos.

```sh
git clone https://github.com/Heitorsv001/Crowns_tlp2.git
cd Crowns_tlp2
mvn compile
mvn javafx:run
```

O plugin aponta para `com.mycompany.crowns.App`. Os comandos seguem a configuração existente, mas não foram executados porque JDK e Maven não estão disponíveis no ambiente da revisão. A compilação Java, isoladamente, não valida o carregamento das telas FXML; considere as pendências acima antes de uma demonstração.

## Verificação e apresentação

Seis arquivos FXML passaram pela validação XML; `creditos.fxml` falhou por conteúdo truncado. Não há testes automatizados versionados. As imagens são recursos do jogo, sem capturas de tela identificadas.

Este repositório é útil como registro de um protótipo. Para apresentação do jogo no portfólio, prefira avaliar o repositório [Crowns](https://github.com/Heitorsv001/Crowns), considerando também suas limitações documentadas.

Mantido na conta [Heitorsv001](https://github.com/Heitorsv001). Repositório original: [Heitorsv001/Crowns_tlp2](https://github.com/Heitorsv001/Crowns_tlp2).
