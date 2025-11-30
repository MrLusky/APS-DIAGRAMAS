# 🗂️ Diagrama de Sequência — *Prime Language*

Este diagrama representa a **interação entre o Aluno, a interface (Site/App), o SystemController e o Banco de Dados**, descrevendo de forma temporal **como os eventos acontecem passo a passo** durante o fluxo de: *Cadastro; Login; Trilhas; Atividades; Comunidade (adicionar amigos ou mandar mensagem) e WordGuess - Nosso jogo de palavras*.

Enquanto o diagrama de atividade mostra *como o fluxo acontece*, o **diagrama de sequência mostra exatamente *quem conversa com quem*, em qual ordem e com qual propósito***.

---

## 🎯 Objetivo do Diagrama

O objetivo deste diagrama é **documentar a comunicação entre os componentes do sistema**, destacando:

- A ordem cronológica das ações.  
- As mensagens enviadas pelo Usuário e pelo Sistema.  
- As validações internas realizadas pelo controller.  
- As consultas e atualizações ocorridas no Banco de Dados.  
- As respostas (reply) devolvidas a cada etapa.  
- As condições alternativas de fluxo (via blocos `alt`).  
- As repetições de tentativas (via blocos `loop`).  

Este diagrama permite entender com precisão **como o sistema reage às ações do aluno**, facilitando desenvolvimento, correção, manutenção e expansão do projeto.

---

## 🧩 Componentes Representados

| Elemento                  | Significado                                                                 |
|--------------------------|------------------------------------------------------------------------------|
| **Lifelines**            | Representam os participantes da interação (Aluno, Site/App, Controller, BD). |
| **Messages**             | Ações iniciadas por algum participante (setas cheias).                       |
| **Reply Messages**       | Respostas a uma ação anterior (setas tracejadas).                            |
| **Activation Bars**      | Período em que um participante está processando uma ação.                    |
| **Alt Frames**           | Representam caminhos alternativos (ex.: válido / inválido).                  |
| **Loop Frames**          | Representam repetições até uma condição ser atingida.                        |
| **Notas**                | Explicações textuais opcionais sobre o comportamento interno.               |

---

## 🔄 Fluxo Principal

O fluxo segue a ordem cronológica exata das mensagens trocadas entre os componentes.

### 🔹 1. Ação inicial  
Descreve o que o aluno faz para iniciar o processo.

### 🔹 2. Comunicação entre Interface → Controller  
Define qual solicitação é enviada e qual tarefa é requisitada.

### 🔹 3. Comunicação Controller → Banco de Dados  
Validações, buscas, atualizações ou verificações.

### 🔹 4. Reply  
O Banco retorna a informação e o Controller devolve o resultado à interface.

### 🔹 5. Exibição ao Usuário  
O Site/App mostra ao aluno o resultado correspondente (sucesso, erro, alerta, progresso etc.).

---

## 🔀 Caminhos Alternativos (`alt`)

O diagrama contempla **condições alternativas**, como:

- Dados inválidos  
- Palavra inexistente  
- Usuário não encontrado  
- Tentativas esgotadas  
- Ação bem-sucedida vs. mal-sucedida  

Cada alternativa é representada por um bloco `alt`, deixando claro como o sistema reage a cada cenário.

---

## 🔁 Repetições (`loop`)

Quando o processo envolve repetição — como:

- Tentativas de adivinhar palavra (WordGuess)  
- Envio de respostas em atividades  
- Interações sucessivas em um chat  

O bloco `loop` define:

- A condição da repetição  
- O conteúdo que se repete  
- Quando o laço é encerrado

---

## 🧵 Finalização do Fluxo

O processo termina quando:

- O aluno recebe o feedback final  
- O sistema conclui as validações  
- Todos os dados necessários são salvos  

Ao final, o diagrama deixa claro **quem encerra a comunicação e como o processo termina**.

---

## 🖼️ Visualização do Diagrama

Abaixo está a representação gráfica do diagrama de sequência:

> *(Inserir aqui a imagem gerada no Astah, via upload no GitHub.)*

