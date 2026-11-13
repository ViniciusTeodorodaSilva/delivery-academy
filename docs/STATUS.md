# STATUS — Delivery Academy

**Atualizado em:** 2026-11-09  
**Etapa atual:** Etapa 0 — fundamentos do ambiente e colaboração  
**Status:** Dois commits locais confirmados: `fc33bc9` e `00a06f8`. Documentação versionada localmente. Publicação no GitHub pendente.

## O que está confirmado

- [x] Referência definida: vídeo `283412.mp4` (24,03 s; 721 quadros; 30 FPS).
- [x] Análise e especificação inicial do app Foodie documentadas em `docs/PLANO_MESTRE.md`.
- [x] Direção pedagógica: aluno desenvolve do zero com autonomia progressiva.
- [x] Stack planejada: Java 21, Spring Boot, PostgreSQL/JDBC/Flyway, React Native/Expo (JSX) e React/Vite para painéis web.
- [x] Regra de continuidade documentada: consultar Plano Mestre, STATUS e AGENTS antes de cada etapa.

## O que NÃO foi confirmado ou feito

- [ ] Repositório `delivery-academy` criado no GitHub.
- [x] Repositório Git **local** inicializado em `C:\Users\vinic\delivery-academy` com `git init -b main` (saída fornecida na conversa em 2026-11-09). `git status`: `On branch main`, `No commits yet`, `exercicios/` untracked; ainda **primeiro commit local confirmado; remoto ainda inexistente/não verificado**.
- [ ] Arquivos deste pacote publicados no GitHub.
- [x] Aluno verificou com `git status --short --untracked-files=all`: `?? .gitignore` e `?? exercicios/java/OlaMundo.java`; com `git status --ignored --short --untracked-files=all`: também `!! exercicios/java/OlaMundo.class`. Evidência: saída literal compartilhada em 2026-11-09.
- [x] Desafio 05 respondido: `.java` é o código do aluno e `.class` é um arquivo gerado; feedback: `.class` é artefato compilado, não necessariamente temporário, mas regenerável.
- [x] `git add .gitignore exercicios/java/OlaMundo.java` executado e confirmado pelo aluno; `git status` mostrou ambos em `Changes to be committed`, e `git diff --cached --name-only` listou somente esses arquivos. **Primeiro commit confirmado posteriormente: `fc33bc9`.**
- [x] Desafio 06 conceitual aprovado: aluno explicou que `git add` prepara e `git commit` registra; corrigida a distinção entre commit local, push e PR/merge (PR não é necessário para primeiro commit direto na main local).
- [x] `.gitignore` local criado na raiz com `*.class`; aluno confirmou `git check-ignore -v exercicios/java/OlaMundo.class` → `.gitignore:1:*.class    exercicios/java/OlaMundo.class`; arquivo compilado ignorado. Os arquivos `.gitignore` e `OlaMundo.java` foram incluídos no primeiro commit local `fc33bc9`.
- [x] Ferramentas e espaço livre conferidos pelo aluno no PowerShell (saída enviada na conversa em 2026-11-08).
- [x] Desafio 07 respondido corretamente: `git commit` grava histórico local persistente mesmo após desligar o computador, mas ainda não publica no GitHub; publicação requer remoto e `git push`. **Execução de `git commit` comprovada na sessão seguinte.**
- [ ] Android Studio e emulador configurados.
- [x] Exercício conceitual linguagem × editor respondido pelo aluno em 2026-11-08; feedback fornecido: VS Code não compila Java por si, o JDK fornece `javac` e a JVM executa bytecode.
- [x] Desafio 02 respondido: confirmou que Java pode ser executado via PowerShell sem VS Code; entendeu necessidade de chamar ferramentas; distinção entre terminal e editor reforçada.
- [x] Compilador Java `javac 21.0.6` confirmado no PowerShell pelo aluno.
- [x] Primeiro programa `OlaMundo.java` criado, compilado e executado pelo aluno em 2026-11-08: `javac OlaMundo.java` sem erros; `java OlaMundo` imprimiu `Meu primeiro programa Java!`; `Get-ChildItem` confirmou `OlaMundo.java` (145 bytes) e `OlaMundo.class` (437 bytes).
- [x] Desafio 03 respondido conceitualmente; aluno confirmou que `java OlaMundo` mostrou a mensagem antiga antes da recompilação e a nova depois de chamar `javac`. **Confirmação por relato do aluno; transcrição do terminal não foi compartilhada.**
- [ ] Backend ou app funcional implementado/testado.

## Próxima aula (Etapa 0)

1. Aula 02: `git init -b main` e `git status` **concluídos e confirmados**; explicar branch, untracked e commits.
2. **Próxima prática:** incorporar `README.md`, `AGENTS.md`, `docs/PLANO_MESTRE.md`, `docs/STATUS.md`, `docs/DECISOES.md` ao repositório local, a partir do pacote de documentação atualizado. Revisar `git status` antes de preparar o segundo commit. **Primeiro commit `fc33bc9` e árvore de trabalho limpa já confirmados.**
3. Publicar documentação no GitHub de forma orientada, praticando commits e PRs.
4. Preparar Android Studio / Android Emulator conforme as condições reais do notebook.
5. Introduzir JavaScript, React Native, Spring Boot e PostgreSQL em exemplos pequenos.

## Critério de aprovação da Etapa 0

Aluno explica Java vs JavaScript, React Native vs Spring Boot, PostgreSQL, Git, SDK e emulador; executa ambiente mínimo, resolve um erro simples, faz commit e demonstra que entende a sequência. **Não marcar como aprovado antes de evidência real.**

## Evidências de ambiente (saída enviada pelo aluno em 2026-11-08)

| Ferramenta / medida | Resultado | Estado |
|---|---|---|
| Git | `2.54.0.windows.1` | Disponível |
| Java | Temurin OpenJDK `21.0.6` LTS, 64 bits | Disponível |
| Node.js | `v24.21.0` | Disponível |
| npm | `11.19.0` (`npm.cmd`) | Disponível |
| Compilador Java | `javac 21.0.6` | Disponível (verificado no PowerShell) |
| Unidade C: | 232,87 GB usados; **705,13 GB livres** | Espaço suficiente para iniciar instalação do Android Studio/SDK/emulador |

*Escopo da validação:* resultados vistos na saída do PowerShell compartilhada; instalações de Android Studio, SDK, emulador e GitHub remoto **não foram verificadas**. Espaço livre não comprova capacidade de virtualização, que será avaliada ao configurar o emulador.

## Registro de sessões

| Data | Sessão | Evidência / progresso | Próximo passo |
|---|---|---|---|
| 2026-11-08 | Planejamento e regra de continuidade | Plano Mestre v1.1 e arquivos de governança preparados localmente; GitHub ainda não verificado | Diagnóstico do PowerShell e publicação guiada |
| 2026-11-08 | Aula 01 — diagnóstico do ambiente | Git, Java, Node, npm e espaço C: confirmados pela saída enviada; 705,13 GB livres | Responder exercício conceitual; depois Git local/documentação e Android Emulator |
| 2026-11-08 | Aula 01 — Desafio 01 | Aluno identificou Java como linguagem e VS Code como ambiente de escrita; confundiu editor/IDE com compilador; foi explicado `javac` → bytecode → JVM | Recuperação ativa; sem afirmar domínio ainda |
| 2026-11-08 | Aula 01 — `javac` | Aluno enviou resultado `javac 21.0.6` no PowerShell; compilador disponível | Responder Desafio 02 com palavras próprias: Java funciona fora do VS Code? Por quê? |
| 2026-11-08 | Aula 01 — Desafio 02 | Aluno explicou corretamente que programas Java podem executar via PowerShell sem VS Code e que o terminal invoca as ferramentas. | Criar e executar `OlaMundo.java` |
| 2026-11-08 | Aula 01 — Prática 01: Hello World | Aluno criou pastas e `OlaMundo.java`, compilou com `javac`, executou com `java`, obteve saída correta e encontrou os arquivos `.java` e `.class`. Resposta conceitual identificou comandos, mas deve reforçar que `javac` compila para bytecode e `java` carrega a classe na JVM. | Experimento de edição/recompilação; explicar por que a saída fica antiga sem novo `javac` |

| 2026-11-08 | Aula 01 — Desafio 03: recompilação | Aluno explicou corretamente que sem `javac` a alteração em `OlaMundo.java` não aparece na execução; entendimento conceitual validado. Ainda não enviou os dois resultados do terminal, por isso a Prática 02 permanece não verificada. | Enviar saídas reais antes/depois da recompilação; em seguida iniciar a próxima prática curta de Git |

## Formato obrigatório de atualização após cada aula

- **Data e objetivo:**
- **O que o aluno fez sozinho:**
- **O que foi testado e evidências:**
- **Lacunas / dificuldades:**
- **Arquivos e commits alterados:**
- **Estado atual e próximo exercício:**


| 2026-11-09 | Aula 01 — conclusão do experimento de recompilação | Aluno relatou que `java OlaMundo` apresentou a mensagem antiga antes de compilar e a mensagem nova depois de `javac`; Desafio 03 aprovado por explicação e relato. Não foi anexado log de saída literal. | Aula 02: `git init` e `git status` na pasta `delivery-academy` |

| 2026-11-09 | Aula 02 — Git local inicializado | Aluno executou `cd "$HOME\delivery-academy"`, `git init -b main` e `git status`; confirmação de branch `main`, sem commits, diretório `exercicios/` untracked. Desafio 04: distinção Git/GitHub e colaboração explicada; ressalva de que Git não elimina automaticamente conflitos. **GitHub ainda não publicado.** | Criar `.gitignore` com `*.class`, verificar quais arquivos são ignorados, praticar staging depois |

| 2026-11-09 | Aula 02 — `.gitignore` validado | Aluno criou `.gitignore` na raiz, inseriu `*.class`; `git check-ignore -v` confirmou regra na linha 1 e arquivo `.class` ignorado. `git status` mostra `.gitignore` e `exercicios/` não rastreados. **Desafio 05 (explicar fonte vs compilado) ainda não respondido.** | Inspecionar `git status --short --untracked-files=all` e `git status --ignored --short --untracked-files=all`; responder Desafio 05; depois staging e primeiro commit |

| 2026-11-09 | Aula 02 — arquivos ignorados e Desafio 05 | Aluno enviou saída real de `git status --short --untracked-files=all` (`?? .gitignore`, `?? exercicios/java/OlaMundo.java`) e de `git status --ignored --short --untracked-files=all` (`!! exercicios/java/OlaMundo.class`). Explicou corretamente fonte vs artefato gerado; registrar nuance de que `.class` não é necessariamente temporário, mas pode ser regenerado. **Primeiro commit confirmado posteriormente: `fc33bc9`.** | Praticar staging com `git add` seletivo e inspecionar antes do primeiro commit |

| 2026-11-09 | Aula 02 — Desafio 06 (staging vs commit vs PR) | Aluno explicou corretamente que `git add` prepara e falta o `git commit` para registrar; trouxe PR/merge como integração à main. Corrigido: PR não é obrigatório, `git push` publica commits quando há remoto, PR propõe integração entre branches. **Posteriormente, execução dos comandos de staging foi confirmada pelo aluno.** | Aluno executar esses três comandos e enviar resultados antes do primeiro commit |

| 2026-11-09 | Aula 02 — staging validado | Aluno executou `git add .gitignore exercicios/java/OlaMundo.java`; `git status` mostrou os dois arquivos como `new file` em `Changes to be committed`; `git diff --cached --name-only` confirmou a seleção. Nenhum commit/push/GitHub validado. | Efetuar primeiro commit local e conferir `git status` e `git log -1 --oneline`; depois preparar documentos iniciais para segundo commit e publicação futura |

| 2026-11-09 | Aula 02 — Desafio 07 (commit local x GitHub) | Aluno respondeu que o commit fica no repositório local ao desligar o notebook e só vai ao GitHub após `git push`. Resposta conceitual aprovada. **Commit confirmado depois, `fc33bc9`**, sem remoto ou push confirmado. | Executar `git commit -m "chore: inicia repositorio com exercicio Java e gitignore"`, `git status`, `git log -1 --oneline`; enviar saídas para validação. |

| 2026-11-09 | Aula 02 — primeiro commit local confirmado | Aluno executou `git commit -m "chore: inicia repositorio com exercicio Java e gitignore"`; Git retornou `[main (root-commit) fc33bc9]`, dois arquivos criados (`.gitignore` e `exercicios/java/OlaMundo.java`), nove inserções. **Sem saída de `git status`/`git log` ainda; sem publicação no GitHub.** | Executar `git status` e `git log -1 --oneline`; validar e preparar a inclusão da documentação de continuidade como segundo commit local. |

| 2026-11-09 | Aula 02 — Desafio 09 e Git status/log validados | Aluno executou `git status`: `On branch main`, `nothing to commit, working tree clean`. `git log -1 --oneline`: `fc33bc9 (HEAD -> main) chore: inicia repositorio com exercicio Java e gitignore`. Explicou que sem novas alterações não há nada para registrar e que arquivos modificados seriam detectados pelo Git. Feedback: `nothing to commit` não significa ausência de commits. | Copiar documentação preparada para o repositório local; inspecionar `git status` antes do segundo commit. |

## Atualização — 09/11/2026

- Primeiro commit Java: `fc33bc9`.
- Segundo commit de documentação: `00a06f8`.
- Plano Mestre v1.1 incluído no repositório local.
- Desafio 10 concluído.
- Próximo passo: publicar o projeto no GitHub.
