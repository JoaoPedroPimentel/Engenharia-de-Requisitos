## Equipe

- Nicolle Da Silva Coelho
- Victor Gabriel Madeiro Brito Marques
- João Pedro Pimentel De Freitas

# Sistema de Desperdício de Alimentos em Mercados

Aplicativo que conecta estabelecimentos que possuem alimentos próximos do vencimento a consumidores interessados em adquiri-los com 50% de desconto, reduzindo o desperdício. Os alimentos não vendidos podem ser destinados a ONGs e instituições parceiras.

Projeto da disciplina de Engenharia de Requisitos, curso de Bacharelado em Engenharia de Software, Centro Universitário de Brasília (CEUB), Novembro de 2026.

## Objetivo

Transformar o desperdício em benefícios econômicos para os comerciantes, economia para os consumidores e impactos sociais e ambientais positivos, tratando problemas como as perdas financeiras de padarias, cafés, restaurantes e supermercados, a dificuldade de acesso a refeições de qualidade por preços mais acessíveis, a burocracia e a falta de logística para doações e a ausência de controle eficiente dos prazos de validade.

## Público-alvo

- **Consumidores:** estudantes e jovens adultos que querem economizar e se preocupam com a causa ambiental.
- **Estabelecimentos:** donos de padarias, cafés, restaurantes e supermercados de pequeno e médio porte.
- **ONGs e instituições parceiras:** bancos de alimentos, asilos e entidades sociais que recebem doações.
- **Administrador da plataforma:** equipe responsável pela gestão do aplicativo.

## Escopo

**O sistema contempla:** cadastro e autenticação de consumidores, estabelecimentos e ONGs, com controle de acesso por perfil; publicação de ofertas com desconto padrão de 50%; cadastro de produtos por lote, com alertas de vencimento; busca de ofertas por localização, categoria, preço e horário, em lista e mapa; reserva e pagamento pelo aplicativo, com retirada por código ou QR Code; módulo de doação com registro e comprovante; gestão financeira (comissão de 10% a 15% por venda concluída e planos de assinatura); relatórios de desperdício, painéis de métricas e indicadores de impacto; notificações, avaliações, favoritos, suporte e denúncia.

**Fora do escopo:** entrega de alimentos em domicílio, venda de produtos fora do prazo de validade, transporte e logística das doações, substituição dos sistemas de estoque ou caixa dos estabelecimentos (a integração é opcional) e gestão de compras e reposição.

## Requisitos

O projeto tem 36 requisitos funcionais (RF01 a RF36) e 22 não funcionais (RNF01 a RNF22), descritos no documento do projeto. Entre os principais requisitos não funcionais:

- Reservar em no máximo 3 toques e publicar uma oferta em no máximo 3 telas.
- Telas principais em até 3 segundos em 4G e busca em até 2 segundos.
- Disponibilidade de no mínimo 99% ao mês e backup diário.
- Conformidade com a LGPD, dados criptografados e pagamento por gateway certificado (PCI-DSS).
- Funcionamento em Android e iOS e painel do estabelecimento acessível pelo navegador.
- Código modular e documentado.

## Arquitetura

A arquitetura é organizada em camadas:

1. **Clientes:** app do consumidor, app do comércio, portal da ONG e painel do administrador.
2. **API Gateway e autenticação:** HTTPS/TLS, login e controle de acesso por perfil.
3. **Back-end modular:** ofertas e lotes (descontos de 50%), busca e mapa, reservas (retirada por QR), pagamentos (comissão de 10% a 15%), doações e comprovantes, notificações (push e alertas), relatórios (perdas e impacto) e admin e suporte (aprovação e CNPJ).
4. **Camada de dados:** banco de dados relacional, cache (busca e estoque), armazenamento (fotos e arquivos) e auditoria (logs e backup).
5. **Integrações externas:** gateway de pagamento (PCI-DSS), mapas e geolocalização, notificações push e Receita Federal (validação de CNPJ).

## Documentação

O documento do projeto reúne introdução, requisitos, arquitetura, protótipo de telas, padrões de design e os diagramas de casos de uso, classes, sequência e entidade-relacionamento. Está na pasta [`docs/`](docs/):

- [`docs/Projeto_Engenharia-de-Requisitos.docx`](docs/Projeto_Engenharia-de-Requisitos.docx)

## Gestão de tarefas

O projeto usa **Kanban**, montado no Miro, que todos os integrantes podem consultar e atualizar: [inserir link do quadro]

Cada cartão representa uma tarefa e contém título começando com verbo, requisito relacionado (por exemplo, RF12 e RF13), responsável e prazo, etiquetas de tipo (documentação, design, requisitos, validação) e de perfil atendido (usuário, estabelecimento, ONG, administrador) e o critério de pronto.

## Padrões de código

Código comentado e padronizado, seguindo boas práticas e convenções, e organizado de forma modular.
