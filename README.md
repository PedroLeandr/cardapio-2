# Cardápio V2

**SaaS de menus digitais para restaurantes, desenvolvido de raiz como projeto pessoal de Back-End e potencial negócio.**

> **Estado:** planeamento. As funcionalidades descritas abaixo são objetivos, não funcionalidades já implementadas.

## Sobre o projeto

O **Cardápio V2** permite que restaurantes criem e atualizem um menu digital sem precisarem de conhecimentos técnicos. Cada restaurante terá um painel de administração e um menu público acessível através de um link ou QR Code.

O projeto tem três objetivos:

1. **Aprender:** aplicar, com autonomia, os conhecimentos do percurso *Back-End Engineer* da Codecademy.
2. **Construir portfólio:** desenvolver uma aplicação real, com API, base de dados, autenticação, testes e deploy.
3. **Validar um negócio:** testar a procura junto de restaurantes antes de investir em funcionalidades avançadas ou publicidade.

O Cardápio anterior serve **apenas de referência visual e funcional**. A V2 será implementada passo a passo, com código escrito e compreendido por mim.

## Problema que queremos resolver

Atualizar menus em papel ou ficheiros estáticos pode ser demorado. O Cardápio V2 pretende tornar simples a edição de produtos, descrições, imagens e preços, com alterações refletidas no menu público.

**Público-alvo inicial:** restaurantes, cafés e pequenos estabelecimentos em Portugal.

## MVP (primeira versão)

### Área do restaurante

- [ ] Criar conta e iniciar/terminar sessão.
- [ ] Criar e editar os dados do restaurante (nome, descrição, identidade visual básica).
- [ ] Criar, editar, ordenar e eliminar categorias.
- [ ] Criar, editar e eliminar produtos (nome, descrição, preço e imagem).
- [ ] Marcar produtos como disponíveis ou indisponíveis.
- [ ] Pré-visualizar o menu antes de o partilhar.
- [ ] Obter link público e QR Code.

### Menu público

- [ ] Página própria de cada restaurante, identificada por um `slug`.
- [ ] Layout responsivo, com prioridade aos telemóveis.
- [ ] Listagem de categorias, produtos, preços e imagens.
- [ ] Apresentação clara de produtos indisponíveis.
- [ ] Acesso sem necessidade de registo.

### Qualidade e segurança

- [ ] Isolar os dados de cada restaurante: um utilizador não pode alterar o menu de outro.
- [ ] Validar os dados recebidos pela API.
- [ ] Guardar palavras-passe com *hash* seguro; nunca em texto simples.
- [ ] Proteger rotas administrativas e tratar erros de forma consistente.
- [ ] Testar os fluxos principais e as permissões.
- [ ] Preparar publicação com HTTPS, configuração segura e cópias de segurança.

## Fora do MVP

Estas funcionalidades só serão consideradas depois de recolher feedback de restaurantes:

- Pedidos online e entregas.
- Reservas de mesas.
- Integração com POS e faturação.
- Pagamentos e subscrições automáticas.
- Estatísticas avançadas.
- Múltiplos temas e personalização detalhada.

## Stack prevista

| Camada | Tecnologia |
| --- | --- |
| Front-End | Next.js, React, TypeScript e CSS |
| Back-End | Node.js, Express e TypeScript |
| Base de dados | MariaDB e SQL |
| Controlo de versões | Git e GitHub |
| Testes | A escolher durante a implementação |
| Infraestrutura | Deploy e Docker numa fase posterior |

**Princípio:** começar simples. Não introduzir Redis, microsserviços ou outras ferramentas sem uma necessidade concreta.

## Estrutura prevista

```text
cardapio-v2/
├── frontend/       # Menu público e painel de administração
├── backend/        # API REST, regras de negócio e acesso à BD
├── docs/           # Requisitos, decisões técnicas e esquemas
└── README.md
```

> A estrutura pode evoluir durante o desenvolvimento. Ainda não existem instruções de instalação porque as aplicações não foram inicializadas.

## Modelo de dados inicial

- **restaurants:** identificação do estabelecimento, `slug` e configurações básicas.
- **users:** conta do responsável e associação ao restaurante.
- **categories:** categorias pertencentes a um restaurante e respetiva ordem.
- **products:** produtos associados a uma categoria, com descrição, preço e disponibilidade.
- **product_images:** referência aos ficheiros das imagens, se necessário.

As relações, restrições, índices e regras de eliminação serão definidos antes da implementação da API.

## Roadmap

- [ ] **Fase 1 | Preparação:** repositório, requisitos, estrutura e primeira página pública com dados fictícios.
- [ ] **Fase 2 | SQL:** modelo relacional, criação das tabelas e consultas essenciais.
- [ ] **Fase 3 | API REST:** operações CRUD de categorias e produtos.
- [ ] **Fase 4 | Autenticação:** login, permissões e isolamento por restaurante.
- [ ] **Fase 5 | Integração:** painel ligado à API, menu público e QR Code.
- [ ] **Fase 6 | Qualidade:** testes, tratamento de erros, segurança básica e deploy.
- [ ] **Fase 7 | Validação:** demonstrações a restaurantes, recolha de feedback e primeiros pilotos.

As fases não têm prazos fixos: o objetivo é compreender e concluir cada etapa antes de avançar.

## Aprendizagem e desenvolvimento

O desenvolvimento acompanha o percurso da **Codecademy – Back-End Engineer**:

| Conteúdo estudado | Aplicação no Cardápio |
| --- | --- |
| JavaScript / TypeScript | Funções, validações e regras de negócio |
| Node.js e Express | Servidor e endpoints REST |
| SQL | Armazenamento e consulta dos menus |
| Autenticação | Acesso ao painel administrativo |
| Testes | Verificação de funcionalidades e permissões |
| Deploy | Publicação e manutenção do serviço |

### Regras pessoais

1. Escrever o código por iniciativa própria.
2. Utilizar IA preferencialmente para explicações, revisão e identificação de erros.
3. Conseguir explicar as decisões técnicas e as funcionalidades implementadas.
4. Dar prioridade à compreensão e à manutenção, não à velocidade de implementação.
5. Fazer commits pequenos e descritivos.

## Validação comercial

**Hipótese inicial de preço:** 19,90 €/mês por restaurante, sujeita a validação.

Plano inicial:

1. Mostrar uma demonstração funcional a restaurantes.
2. Contactar cerca de 20 estabelecimentos e identificar as objeções mais frequentes.
3. Tentar obter 3 clientes piloto.
4. Rever produto e preço com base no interesse real e na disposição para pagar.
5. Só depois avaliar campanhas pagas de marketing.

Este preço é uma hipótese, não uma promessa de vendas ou de rentabilidade.

## Próximos passos

- [ ] Criar o repositório `cardapio-v2`.
- [ ] Adicionar este `README.md`.
- [ ] Criar as pastas `frontend`, `backend` e `docs`.
- [ ] Desenhar as páginas e os fluxos principais.
- [ ] Definir o diagrama inicial da base de dados.
- [ ] Fazer o primeiro commit.

---

**Objetivo final:** lançar um produto que consiga manter sozinho, com potencial para clientes reais, e demonstrar competências sólidas de desenvolvimento Back-End.
