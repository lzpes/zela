# Zela

**Zelando pela sua cidade.**

Zela é um aplicativo de zeladoria urbana que conecta o cidadão à gestão pública. O morador registra problemas da cidade (buraco na rua, iluminação falhando, lixo em local inadequado) com foto e localização exata no mapa, e acompanha cada etapa até a resolução. Para a gestão pública, o Zela centraliza as ocorrências em um painel com indicadores, gráficos e mapas de calor.

Projeto desenvolvido no curso de Engenharia de Software do Centro Universitário UNICEPLAC, em parceria com a Stefanini Consultoria e Assessoria em Informática S.A.

## Problema

Apontar um problema urbano hoje costuma ser um processo burocrático e fragmentado: as informações se perdem em vários canais, falta localização precisa e o cidadão não sabe se o pedido foi atendido. A gestão pública, por sua vez, perde a visão do todo e a capacidade de priorizar o que é mais urgente.

## Funcionalidades

**Cidadão**
- Cadastro e autenticação (e-mail/CPF e senha, login social com Google e Facebook)
- Registro de ocorrência com foto, categoria, descrição e localização via GPS
- Acompanhamento do status: Registrada, Em Análise, Em Execução, Concluída
- Mapa interativo com as ocorrências da região
- Notificações push sobre mudanças de status

**Gestor público**
- Painel administrativo com indicadores e estatísticas
- Mapas de calor para identificar áreas críticas
- Gestão e atualização de status das ocorrências, com comentários

## Arquitetura

| Camada | Tecnologia |
|---|---|
| App mobile (Android e iOS) | React Native |
| API / Back-end | Node.js + Express (REST, HTTPS/JSON) |
| Banco de dados | PostgreSQL + PostGIS + pgcrypto |
| Integrações | Google Maps API, Firebase Storage, Firebase Cloud Messaging |

### Modelo de dados (DER)

Entidades principais: Usuario, Endereco, Ocorrencia, CategoriaOcorrencia, StatusOcorrencia, HistoricoStatusOcorrencia, MidiaOcorrencia, Dispositivo, UsuarioDispositivo, Conta e Banco.

O banco já conta com as tabelas `users`, `refresh_tokens` e `password_reset_tokens`, validações via CHECK (formato de e-mail e CPF), índices e trigger de auditoria (`updated_at`).

## Estrutura do repositório

```
zela/
├── mobile/      # app React Native
├── backend/     # API Node.js + Express
├── database/    # scripts SQL (schema, migrations, seeds)
├── docs/        # BMC, diagramas (arquitetura e DER), carta de aceite, artigo
└── README.md
```

## Protótipo

Telas de onboarding, login e cadastro no [Figma](https://www.figma.com/design/Wud45Gy2EvNUAm7SPRkKM1/TELA-LOGIN-E-CADASTRO-ZELA?node-id=237-3584&t=yBUGdc3M2hHpyE8q-0).

## Metodologia

Pesquisa aplicada, qualitativa e exploratória, com desenvolvimento iterativo e incremental inspirado em práticas ágeis, com entregas semanais validadas pelo professor orientador.

Etapas: levantamento de requisitos, Business Model Canvas, modelagem técnica (arquitetura e DER), implementação do banco, prototipação da interface, validação institucional e acompanhamento contínuo.

## Status

- [x] Levantamento de requisitos
- [x] Business Model Canvas
- [x] Diagrama de arquitetura e DER
- [x] Script inicial do banco de dados
- [x] Protótipo: onboarding, login e cadastro
- [ ] API (autenticação e ocorrências)
- [ ] App mobile
- [ ] Painel administrativo
- [ ] Testes de usabilidade

## Como rodar

Em breve, conforme os módulos forem sendo implementados.

## Equipe

Adriano Henrique Gurgel Batalha, Alexandre Alves de Carvalho, Guilherme Lopes Mendes, Lucas Felipe Pereira Amorim, Gabriel da Silva Coelho, Lucas de Moraes Petter, Êllyel Ferreira Alves e Kleber Anderson Betcel Lima.

## Instituição e parceria

- Centro Universitário UNICEPLAC, Engenharia de Software
- Parceira/madrinha: Stefanini Consultoria e Assessoria em Informática S.A.

## Licença

A definir.
