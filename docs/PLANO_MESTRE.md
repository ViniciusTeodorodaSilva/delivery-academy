# Plano Mestre — Delivery Academy

**Versão:** 1.1 — 2026-11-08. **Estado:** planejamento e preparação de ambiente; repositório remoto ainda não confirmado.

**Tipo:** projeto educacional, público no GitHub, construído pelo aluno do zero.  
**Referência:** vídeo enviado `283412.mp4` (24,03 s, 721 quadros, 30 FPS; 720 × 936).  
**Visão:** recriar a experiência visual observada em português e evoluí-la para uma plataforma de delivery Full Stack real, com competência para construir, explicar, testar, operar e manter cada componente sem depender de IA.

## 0. Protocolo obrigatório de continuidade (regra permanente)

**Fonte principal de verdade:** a versão mais recente do arquivo `docs/PLANO_MESTRE.md` na branch principal do **repositório oficial do projeto**, assim que criado e publicado. Não substituir esse documento por memória de conversas, resumos ou palpites. Os documentos deste pacote são a versão inicial a ser levada ao GitHub **pelo próprio aluno durante as aulas**. Até a publicação, estes arquivos locais são uma cópia de preparação, não prova de conteúdo no GitHub.

### Antes de qualquer aula, proposta, implementação ou retomada

1. **Ler o Plano Mestre** atualizado e respeitar seus requisitos, escolhas técnicas, princípios pedagógicos e limites de escopo.
2. **Ler `docs/STATUS.md`** para verificar a última etapa validada, o que foi feito por você, pendências, bloqueios e o próximo exercício.
3. **Ler `AGENTS.md`** antes de usar Codex, Claude ou outro agente. Consultar `docs/DECISOES.md` quando a tarefa envolver decisões ou mudanças de arquitetura/escopo.
4. Comparar o pedido atual com os acordos existentes. **Não reiniciar** o projeto, não apagar requisitos e não trocar tecnologias unilateralmente.
5. Se algum arquivo estiver inacessível, desatualizado ou conflitante, **declarar a limitação e solicitar a versão vigente** em vez de afirmar falsamente que consultou o repositório.

### Depois de qualquer etapa concluída ou decisão nova

1. Atualizar `docs/STATUS.md` com data, etapa, resultado **validado**, tarefas pendentes, próximo passo e evidências (comandos, testes, commit/PR se existirem).
2. Atualizar este Plano Mestre **quando houver alteração de requisito, escopo, ordem de formação, tecnologia, segurança ou metodologia**. Se for apenas avanço normal, atualizar o STATUS sem reescrever o plano.
3. Registrar mudanças relevantes e sua justificativa em `docs/DECISOES.md`; conservar histórico de versões por Git.
4. Criar commit legível na branch apropriada, revisar o diff e publicar via PR conforme o nível da aula. **Não afirmar que houve push, PR ou merge sem verificar.**
5. Finalizar com um resumo de **o que aprendeu**, **o que você consegue reproduzir sem IA** e **o próximo exercício**.

### Estados explícitos para evitar confusão

Usar `[OBSERVADO NO VÍDEO]`, `[PLANEJADO]`, `[EM IMPLEMENTAÇÃO]`, `[IMPLEMENTADO]`, `[TESTADO]`, `[BLOQUEADO]` e `[NÃO VERIFICADO]`. Uma interface mostrada no vídeo **não** comprova backend real; um plano documentado **não** comprova funcionalidade entregue.

### Regra de ensino e autonomia

O aluno escreve os exercícios, responde perguntas, depura e explica os resultados. A IA atua primeiro como **professor/revisor**, com dicas graduais, e só passa a escrever soluções completas quando houver pedido explícito ou quando isso fizer parte da etapa avançada de engenharia de IA. O ritmo depende da compreensão demonstrada, e não de prazos arbitrários.

### Recuperação de contexto em novos chats

Abrir a versão oficial dos arquivos do GitHub, começando por `docs/PLANO_MESTRE.md`, `docs/STATUS.md` e `AGENTS.md`; não presumir que a memória do ChatGPT contém a última atualização. **Se ainda não houver acesso ao GitHub**, pedir o link ou arquivo vigente. O objetivo é continuidade verificável, inclusive com troca de conta, dispositivo ou assistente.

---

## 1. Análise do vídeo — fatos observados

O original é uma gravação do simulador iPhone com o editor aberto mostrando **Dart/Flutter**, `FoodieApp`, `SplashPage`, `ScreenUtilInit` e imports como `package:flutter/material.dart` e `package:flutter/services.dart`. Não há prova de backend nem de processamento real de pagamentos no vídeo.

| Intervalo aproximado | Observação direta | Habilidades para reprodução |
|---|---|---|
| 00:00–00:00,9 | Simulador iOS na tela inicial e abertura do aplicativo | ciclo de vida, inicialização, execução no emulador |
| 00:00,9–00:01,8 | tela clara de transição | navegação, animações e temporização |
| 00:01,8–00:05,3 | splash com entregador de scooter, logo “Foodie.”, slogan | assets, composição, centralização, sequência de animações |
| 00:05,3–00:06,5 | transição com cabeçalho verde e formulário aparecendo progressivamente | animações, layout flexível, transições |
| 00:06,5–00:08 | login completo com e-mail/telefone, senha, manter conectado, esqueci senha, Google/Apple e cadastro | formulários, acessibilidade, validação, componentes reutilizáveis |
| 00:08–00:11,5 | usuário digita e-mail inválido; borda e mensagem vermelhas | estado, eventos, validação, feedback acessível |
| 00:11,5–00:13,8 | e-mail corrigido e senha informada | máscara, mostrar/ocultar, teclado, gerenciamento de estado |
| 00:13,8–00:15,1 | botão de login, carregamento e transição para catálogo | estados de espera/erro, autenticação real futura |
| 00:15,1–00:17 | header com perfil, endereço, banner; categorias e “pedir novamente”, ofertas, restaurantes | navegação, listas horizontais, componentes, imagens |
| 00:17–00:20,35 | rolagem para cartões de restaurantes e produtos (preços, calorias, tempo, botão +) | listas e grids performáticos, carrinho, cache, paginação |
| 00:20,35–00:24,03 | encerramento com sobreposição de rede social | não faz parte das funcionalidades do app |

### Elementos visuais observados

- Paleta predominante: verde limão/oliva, verde floresta, branco e cinza claro.
- Splash: personagem de entregador sobre scooter, fundo off-white, marca centralizada e slogan.
- Login: topo ilustrado com gradiente verde; campos arredondados; ícones; botão em gradiente; divisória; login social; link para cadastro.
- Home: localização e avatar; notificações; banners; ícones de categorias; carrosséis “pedir novamente”, cupons, restaurantes; cartões com preços e tempos.
- Navegação inferior com **cinco abas**: Home, Saved, Cart, Offers e Profile.
- Produtos visíveis: hambúrgueres, pizza, sushi, bebidas, frango, carnes, cachorro-quente etc.; preços em dólar na referência (nossa versão deverá ter formatação pt-BR e moeda configurável).
- O vídeo mostra entrada de dados e rolagem; **não** prova funcionamento de OAuth Google/Apple, checkout, notificações remotas, gestão dos restaurantes ou entrega em tempo real.

## 2. Decisões de tecnologia

| Camada | Tecnologia | Motivo / o que estudar |
|---|---|---|
| Linguagens principais | Java 21 e JavaScript/JSX | reaproveitar conhecimentos dos outros projetos; Java com orientação a objetos e JS para interface |
| Mobile | React Native com Expo | Android/iOS com componentes nativos; ecossistema React e JSX |
| Painéis web | React + Vite + JS/JSX | tecnologia já usada; administração e loja no navegador |
| Backend | Spring Boot + Spring Security | APIs REST, autenticação, regras de negócio, validação, arquitetura |
| Persistência | PostgreSQL + JDBC + Flyway | SQL real, migrações e acesso explícito ao banco; JPA pode ser aprendido como comparação posteriormente |
| Testes | JUnit, testes integrados, React Native Testing Library, Playwright para web | qualidade, regressão, segurança e confiança |
| Infra inicial | Windows + VS Code + Android Studio Emulator + IntelliJ + Docker | desenvolvimento local e emulador ao lado do editor |
| Colaboração | Git + GitHub + Issues + PRs + Actions | trabalho profissional e portfólio |
| AWS (posterior) | IAM, VPC, RDS, S3, ECS/Fargate, CloudWatch, Secrets Manager, orçamento | operação real e conhecimento de cloud |
| IA aplicada (posterior) | APIs de LLM, embeddings/RAG, tool calling, avaliação, agentes, observabilidade | operar IA com controle técnico, segurança e custos |

**Nota:** reproduzir a mesma experiência visual em React Native não é copiar o código Flutter; serão decisões próprias de implementação. A exatidão visual exigirá comparar capturas do nosso emulador com os quadros originais. Use assets próprios, licenciados ou autorizados ao publicar no GitHub.

**Windows:** o Android Emulator funciona no Windows; o simulador oficial de iPhone do Xcode exige macOS. Para testar iOS, usar um dispositivo real ou uma infraestrutura apropriada quando o produto estiver pronto.

## 3. Produto completo planejado (além do vídeo)

**Aplicativo do cliente:** onboarding; cadastro/login; verificação; recuperar senha; conta e endereços; geolocalização opcional; pesquisa e filtros; categorias; restaurantes e avaliações; detalhes e adicionais de produtos; favoritos; promoções e cupons; carrinho; checkout; taxas; pagamentos integrados futuramente; confirmação; acompanhamento de pedido; histórico e repetição; notificações; suporte e acessibilidade; português e inglês; moeda e localidade configuráveis.

**Painel do restaurante:** cadastro de estabelecimento e equipe, produtos/categorias/estoque, preços e adicionais, horários, promoções, fila de pedidos, tempo de preparo e relatórios.

**Experiência de entregador:** aceite de corridas, status, coleta, entrega, histórico e localização com consentimento.

**Administração:** governança, papéis e permissões, moderação, auditoria, catálogo, disputas, configuração de taxas, saúde operacional e métricas.

**Backend:** contas, perfil, autenticação, catálogo, inventário, carrinho, cálculo de preço no servidor, pedidos, pagamentos com integrações reais somente após homologação, notificações, eventos e auditoria. Isolamento multiestabelecimento, autorização por recurso, proteção de dados e idempotência são obrigatórios.

**Princípio de arquitetura:** monólito modular Spring Boot antes de microserviços. Evitar complexidade sem necessidade. Separar domínio, aplicação, API e infraestrutura; usar contratos e testes.

## 4. Trilha de competências por entregas

### Etapa 0 — Fundamentos do ambiente e colaboração

- Entender terminal, diretórios, processos, variáveis de ambiente, SDK, emulador, IDE e diferença entre frontend/backend.
- Instalar/verificar Git, JDK 21, Node, Android Studio, VS Code, IntelliJ, PostgreSQL/Docker.
- Abrir Android Emulator lado a lado com VS Code, executar app inicial, depurar e usar hot reload.
- Criar repositório `delivery-academy`; README, `.gitignore`, commits sem segredos, branch, Issue e PR.
- **Teste de domínio:** explicar cada ferramenta e reconstruir o ambiente com suas próprias anotações.

### Etapa 1 — Programação de verdade

- Algoritmos e pseudocódigo, valores e tipos, variáveis, operadores, condições, loops, funções, escopo, arrays, objetos, módulos, exceções, debug.
- JavaScript assíncrono, promises, async/await; Java classes, interfaces, herança, composição, coleções, generics, Streams, exceções, memória e testes.
- Fazer pequenos exercícios em terminal antes de copiar código de telas.
- **Teste de domínio:** programar soluções similares sem referência e explicar linha por linha.

### Etapa 2 — Git e engenharia de software

- Branches, commits atômicos, conflitos, PR, code review, Issues, documentação, versionamento, Clean Code, SOLID, legibilidade e debugging.
- Ciclo de trabalho real: Issue → branch → implementação → testes → revisão → PR → merge.
- **Teste de domínio:** corrigir um bug introduzido intencionalmente e escrever relato técnico de causa raiz.

### Etapa 3 — UI mobile fiel ao vídeo

- JSX, componentes, props, estado, hooks, estilos, layout flex, tipografia, responsividade, safe areas, assets, animações, navegação, formulários.
- Recriar splash → login → home com textos em português, animações e pontos de interação observados.
- Três estados por recurso: carregando, sucesso e erro; também vazio quando aplicável.
- **Teste de domínio:** recriar uma seção removendo a consulta e explicar o que acontece ao tocar em cada componente.

### Etapa 4 — Back-end profissional

- HTTP, REST, JSON, status codes, headers, API design, validação, logs, testes, tratamento consistente de erros.
- Spring Boot, injeção de dependências, controllers/services/repositories, JDBC, PostgreSQL, Flyway, SQL, índices, joins, transações, constraints.
- Auth real com senha hasheada, sessões/tokens, refresh seguro, recuperação de senha e proteção contra enumeração.
- **Teste de domínio:** implementar endpoint, migration e teste de integração sem receber a solução pronta.

### Etapa 5 — Delivery funcional

- Catálogo persistido, restaurantes, produtos, preços, endereço, pesquisa, carrinho, cupons, cálculo financeiro, checkout de teste e pedido.
- Máquina de estados do pedido: criado → confirmado → em preparo → pronto → em entrega → entregue/cancelado, com transições autorizadas.
- Adicionar módulos de restaurante, entregador e administração em entregas independentes.
- **Teste de domínio:** demonstrar uma jornada ponta a ponta com banco real e explicar cada escrita e leitura.

### Etapa 6 — Produção e qualidade

- Testes unitários, integração, contratos, E2E, acessibilidade, performance, segurança (IDOR/BOLA, autenticação, autorização, LGPD), rate limit, logs, métricas.
- Docker Compose, CI/CD, migrations, backups/restauração, ambientes de desenvolvimento/homologação/produção, observabilidade, alarmes e incidentes.
- **Teste de domínio:** resolver falhas simuladas, recuperar backup, explicar riscos e operar sem dependência de agentes.

### Etapa 7 — AWS e certificações

- Fundamentos: cloud, regiões, zonas, IAM, políticas, MFA, redes, VPC, subnets, segurança, custo.
- Prática: backend em ECS/Fargate ou serviço equivalente; PostgreSQL no RDS; imagens no S3; logs/métricas no CloudWatch; secrets no Secrets Manager.
- Segurança financeira: AWS Budgets/alertas, desligamento de recursos de laboratório, auditoria de uso. Não pressupor que todos os serviços serão gratuitos.
- Certificações possíveis (verificar trilhas oficiais e requisitos vigentes antes de inscrição): Cloud Practitioner opcional → Developer Associate e/ou Solutions Architect Associate → AI Practitioner e, se fizer sentido, Machine Learning Engineer Associate. Níveis Professional posteriormente.
- **Teste de domínio:** explicar rede, IAM, custo, deploy, segurança e recuperação de falhas.

### Etapa 8 — Engenharia de IA

- Entender conceitos: tokens, contexto, probabilidade, transformers, embeddings, limites, alucinação, dados de treino vs inferência.
- Prompting e especificação: objetivos, requisitos, exemplos, critérios de aceitação, formatos de saída e limites.
- Uso técnico de IA: versionamento de prompts, Git, testes, contexto do repositório, revisão de diffs, evidências, avaliação de resultados.
- Desenvolvimento: APIs de LLM, function/tool calling, JSON estruturado, RAG com embeddings e pgvector, recuperação e citações, agentes com permissões limitadas, fluxos de aprovação, evals, testes adversariais, prompt injection e observabilidade.
- Economia: latência, custo por token, caching, escolha de modelos por tarefa, limites, orçamentos e degradação segura.
- **Teste de domínio:** implementar uma funcionalidade com e sem IA, detectar erro gerado por modelo, justificar decisões arquiteturais e medir qualidade/custo.

### Etapa 9 — Evolução de pleno para sênior

- Projetar sistemas com trade-offs, confiabilidade, concorrência, dados, segurança, performance, custo, decisões registradas em ADRs.
- Liderar entregas, estimar riscos, fazer code review útil, ensinar outras pessoas, diagnosticar incidentes, comunicar-se com stakeholders e assumir responsabilidade operacional.
- **Critério:** senioridade vem de competência demonstrada, autonomia, impacto e experiência real sustentada; certificado ou aplicativo isolado não garantem nível sênior.

## 5. Método de aula

1. O professor explica um conceito curto, por que ele existe e apresenta exemplo mínimo.
2. O aluno digita código e raciocina sozinho; nada de colar uma aplicação pronta sem entender.
3. Mini desafio sem consultar a solução; feedback e pistas graduais quando necessário.
4. Executar, debugar, testar e fazer commit; explicar o funcionamento com palavras próprias.
5. Retomar o conhecimento 1, 7 e 30 dias depois, misturando conceitos já estudados.
6. Quando houver domínio independente, repetir o exercício com Codex/Claude como auxiliares e revisar o trabalho deles.

### Porta de aprovação entre etapas

- Explicar o código e o fluxo sem consulta.
- Alterar a funcionalidade de modo independente.
- Encontrar e corrigir erro deliberado.
- Criar teste adequado e fazer commit explicável.
- Só então avançar; se ainda houver lacunas, reforçar o conceito.

## 6. Estrutura inicial de repositório (planejada, NÃO criar tudo na primeira aula)

```text
delivery-academy/
  README.md
  AGENTS.md
  docs/
    PLANO_MESTRE.md     # fonte principal de verdade
    STATUS.md            # ponto exato para retomar
    DECISOES.md          # histórico de decisões
    analise-video.md     # opcional, no momento oportuno
    trilha-estudos.md    # opcional, no momento oportuno
  mobile/          # React Native / Expo (JSX)
  backend/         # Spring Boot / Java
  admin-web/       # React / Vite
  infra/           # compose, scripts e deploy
  .github/         # templates, actions, automações seguras
```

Começar com **README, Git e os documentos mínimos de continuidade** (`PLANO_MESTRE.md`, `STATUS.md`, `DECISOES.md`, `AGENTS.md`). As pastas de código surgirão conforme a necessidade; o próprio aluno criará e versionará o repositório durante as aulas.

## 7. Primeira sessão de trabalho

**Meta:** preparar um ambiente em que você veja o emulador Android ao lado do VS Code e entenda o papel de cada peça.

No PowerShell, digitar e interpretar (não executar comandos desconhecidos sem analisar):

```powershell
git --version
java -version
node --version
npm.cmd --version
Get-PSDrive C
```

O `npm.cmd` evita bloqueios comuns do `npm.ps1` no PowerShell. Verificar espaço livre antes do Android Studio, SDK e emulador, pois o conjunto ocupa vários GB.

**Exercício de recuperação:** escrever, de cabeça e com suas palavras, a diferença entre Java, JavaScript, React Native, Spring Boot, PostgreSQL, Git e Android Emulator. O professor corrigirá a explicação.

**Depois:** instalar/configurar Android Studio e criar um aparelho virtual Android; configurar VS Code; só então iniciar o projeto mínimo e aprender a executar, ler erros, usar hot reload e depurar.

## 8. Regras importantes

- O repositório será público para recrutamento; jamais adicionar chaves, senhas, dados reais ou arquivos de configuração secretos.
- Não afirmar funcionalidades como “login Google”, pagamento e notificações funcionais até que sejam implementadas/testadas.
- Não copiar nomes, ilustrações, logos e fotografias protegidos sem licença/permissão; criar assets próprios com visual inspirado na referência.
- Não começar com microserviços ou agentes autônomos sem fundamentos.
- Verificar documentação vigente da AWS e programas de certificação antes de provas ou cobranças; este plano é conceitual, não catálogo atualizado de exames.
- O produto poderá usar português por padrão e estrutura de internacionalização (i18n) para outros idiomas/regiões.

**Próximo marco:** emulador funcionando, repositório inicial documentado e primeira tela explicada linha a linha.
