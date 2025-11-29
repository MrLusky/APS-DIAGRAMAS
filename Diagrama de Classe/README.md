# 🗂️ Diagrama de Atividade — Prime Language

Este diagrama representa o **fluxo de atividades do usuário dentro da plataforma Prime Language**, descrevendo de forma visual **como o aluno navega pelo sistema**, quais caminhos pode seguir, e como as funcionalidades internas são ativadas durante essa navegação.

Enquanto um diagrama de caso de uso mostra *o que* o sistema oferece, o diagrama de atividade descreve *como* esses processos acontecem na prática.

---

## 🎯 Objetivo do Diagrama

O objetivo deste diagrama é **documentar o comportamento do usuário dentro do sistema**, destacando:

- As possíveis escolhas que o aluno pode tomar ao navegar.
- Os diferentes caminhos que um fluxo pode assumir.
- Os pontos onde processos ocorrem em paralelo (ações simultâneas).
- As condições que direcionam o usuário a fluxos distintos.
- O ponto final comum após todas as interações.

Este diagrama é útil para desenvolvedores, designers de lógica, professores da equipe e qualquer membro que precise entender **a dinâmica completa do funcionamento do sistema**.

---

## 🧩 Componentes Representados

| Elemento                   | Significado                                                                 |
| -------------------------- | --------------------------------------------------------------------------- |
| **Atividades**             | Ações realizadas pelo usuário ou pelo sistema (ex.: “Acessar aula”).        |
| **Nós de Decisão**         | Pontos onde o fluxo escolhe um caminho entre alternativas.                  |
| **Merge Nodes**            | Convergem vários caminhos alternativos para um único ponto.                 |
| **Fork Nodes**             | Dividem o fluxo em ações paralelas que ocorrem simultaneamente.             |
| **Join Nodes**             | Aguardam ações paralelas terminarem para continuar o fluxo.                 |
| **Activity Final Node**    | Representa o encerramento do processo.                                      |

---

## 🔄 Fluxo Principal do Sistema

### 🧑‍🎓 **Entrada do Usuário**

O fluxo se inicia quando o aluno acessa o sistema.  
Ele pode:

- Acessar página de cursos  
- Selecionar curso  
- Acessar aula  
- Jogar WordGuess  
- Acessar trilhas  
- Acessar atividades  
- Acessar comunidade  
- Acessar perfil  

Caso o aluno **não possua conta**, é direcionado ao cadastro.  
Caso **possua conta**, segue para o login.

---

## 🧭 Navegação Dentro do Sistema

Após logado, o usuário pode seguir diferentes caminhos independentes:

- Acessar trilhas de aprendizado  
- Acessar comunidade  
  - Se já possui amizade → abrir chat → mandar mensagem  
  - Se não possui → adicionar amigo  
- Acessar atividades  
- Jogar WordGuess  
- Acessar o próprio perfil  
  - Alterar dados pessoais  
  - Salvar mudanças  
  - Deletar conta  

Essas ações são **alternativas** e representadas por nós de decisão e merge, mostrando que o aluno **escolhe um único caminho por vez**.

---

## 🔀 Ações Internas Simultâneas

Ao realizar certas ações — como assistir aula, jogar WordGuess ou realizar atividades — o sistema executa processos internos simultaneamente.

Isso é representado por um **Fork Node**, que divide o fluxo em:

- Adicionar palavras aprendidas  
- Salvar progresso  
- Adicionar +1 à streak (somente se for o primeiro acesso do dia)  

Essas atividades ocorrem **em paralelo**, garantindo atualização completa do progresso.

Posteriormente, um **Join Node** reúne esses caminhos, garantindo que todas as ações tenham sido concluídas antes de encerrar o fluxo.

---

## 🧵 Finalização do Fluxo

Todas as rotas possíveis — independentemente da ação escolhida — convergem para um único **Activity Final Node**, representando o término da interação do usuário.

Isso garante que, mesmo com múltiplas possibilidades e caminhos distintos, **todos os fluxos possuem um encerramento claro e consistente**.

---

## 🖼️ Visualização do Diagrama

Abaixo está a representação gráfica do diagrama de atividade:

