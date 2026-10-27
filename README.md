# Sistema de Gestão e Operações Aéreas

Plataforma para centralizar, automatizar e otimizar os processos críticos de companhias aéreas e centros de controle de operações (OCC): malha aérea, controle de frota, escalas de tripulação, acompanhamento de manutenção, despacho operacional e tratamento de disrupções.

> Status: em fase de especificação (levantamento de requisitos e modelagem).

## Propósito

Ser a única fonte de verdade (Single Source of Truth) para operadores, despachantes, engenheiros de manutenção e tripulantes, reduzindo riscos operacionais, eliminando planilhas desconectadas, agilizando decisões em tempo real e garantindo conformidade com os regulamentos de segurança da aviação civil.

## Objetivos

Geral: projetar e especificar uma arquitetura de software robusta, segura e escalável para o gerenciamento de operações aéreas de grande porte.

Específicos:

- Automatizar o cálculo de combustível e o balanceamento de peso
- Bloquear automaticamente aeronaves com itens de manutenção vencidos
- Validar os limites legais de jornada de tripulantes
- Integrar dados meteorológicos e NOTAM em tempo real
- Prover trilhas de auditoria imutáveis para rastreabilidade regulatória

## Módulos

| Código | Módulo |
|--------|--------|
| RF01 | Gerenciamento do ciclo de vida dos voos |
| RF02 | Registro e status operacional da frota |
| RF03 | Escalonamento de pilotos e comissários |
| RF04 | Manutenção preventiva e corretiva (ordens de serviço e bloqueios) |
| RF05 | Despacho operacional |
| RF06 | Cálculo de combustível |
| RF07 | Consulta meteorológica |
| RF08 | Tratamento de disrupções |
| RF09 | Alertas automáticos |
| RF10 | Relatórios gerenciais de pontualidade (OTP) |
| RF11 | Perfis e acessos (RBAC) |

## Documentação

- [Levantamento de requisitos](docs/requisitos.md)
- [Regras de negócio](docs/regras-de-negocio.md)

## Estrutura do repositório

```
.
├── README.md
├── .gitignore
├── docs/
│   ├── requisitos.md
│   ├── regras-de-negocio.md
│   └── diagramas/        # casos de uso, classes, sequência, etc.
└── src/                  # código-fonte (futuro)
```

## Roadmap

- [x] Visão geral e objetivos
- [x] Levantamento de requisitos
- [ ] Diagrama de casos de uso
- [ ] Diagrama de classes
- [ ] Diagrama de sequência
- [ ] Modelo de dados (DER)
- [ ] Arquitetura da solução
- [ ] Protótipo / implementação

## Licença

A definir.
