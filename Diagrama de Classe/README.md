# 🧱 Diagrama de Classe — Prime Language

Este diagrama de classe representa **a estrutura interna do sistema Prime Language**, mostrando como os dados são organizados, como as entidades se relacionam entre si e quais operações cada classe oferece.

Enquanto outros diagramas mostram o fluxo ou funcionalidades, o diagrama de classe revela **a arquitetura lógica do sistema**, servindo como base para implementação do backend, Banco de Dados e regras de negócio.

---

## 🎯 Objetivo do Diagrama

O objetivo do diagrama é:

- Organizar as entidades principais do sistema.
- Definir atributos e comportamentos de cada classe.
- Representar os relacionamentos entre elas:
  - **Associações**
  - **Cardinalidades**
  - **Dependências**
  - **Agregações/Composições** (quando aplicável)
- Deixar clara a estrutura necessária para:
  - matrículas  
  - lições  
  - testes  
  - progressos  
  - exercícios  
  - comunidade  
  - usuários  

Este diagrama funciona como referência para desenvolvedores, equipe de banco de dados, documentações de API e integrações futuras.

---

## 🧩 Classes Principais

### 🧑‍🏫 **Usuário**
Representa qualquer pessoa cadastrada na plataforma.

**Atributos:**
- id  
- nome  
- email  
- senha_hash  
- data_criacao  
- ultima_atv  

**Métodos:**
- atualizar_perfil()  
- iniciar_teste_nivel()  
- matricular_curso()  

O usuário está ligado a matrículas, tentativas de teste e postagens da comunidade.

---

### 🌐 **Idioma**
Representa os idiomas suportados pelo sistema.

**Atributos:**
- id  
- nome  
- sigla  

Relaciona-se com vários cursos (1:N) e com testes de nível.

---

### 📘 **Curso**
Cada idioma possui cursos específicos.

**Atributos:**
- id  
- idioma_id  
- nome  
- nivel  
- descricao  

**Métodos:**
- listar_licoes()  
- recomendar_proxima_licao()  

Relaciona-se com **Lições** e **Matrículas**.

---

### 📚 **Lição**
Elemento central do aprendizado dentro do curso.

**Atributos:**
- id  
- curso_id  
- titulo  
- ordem  
- tipo  
- duracao  

**Métodos:**
- listar_exercicios()  
- marcar_concluido()  

---

### 📝 **Exercício**
Associado diretamente a uma lição.

**Atributos:**
- id  
- licao_id  
- tipo_exercicio  
- enunciado  
- resposta_correta  
- midia  

**Métodos:**
- corrigir_resposta()  

---

### 🎓 **Matrícula**
Representa o vínculo entre usuário e curso.

**Atributos:**
- id  
- usuario_id  
- curso_id  
- data  
- status  

**Métodos:**
- cancelar()  
- reativar()  

Uma matrícula está ligada às lições concluídas e ao progresso.

---

### 📈 **Progresso**
Registra o avanço de cada usuário nas lições.

**Atributos:**
- id  
- matricula_id  
- licao_id  
- data_atualizacao  

**Métodos:**
- atualizar_status()  

---

### 🧪 **Teste de Nível**
Determina o nível do aluno no idioma.

**Atributos:**
- id  
- idioma_id  
- nome  
- descricao  
- numero_questoes  

**Métodos:**
- gerar_prova()  

---

### 🗳️ **Tentativa de Teste**
Cada realização do teste de nível fica registrada aqui.

**Atributos:**
- id  
- teste_id  
- usuario_id  
- pontuacao  
- data  
- nivel_sugerido  

**Método:**
- calcular_nivel()  

---

### 💬 **Depoimento**
Depoimentos deixados pelo usuário.

**Atributos:**
- id  
- usuario_id  
- texto  
- data  
- nota  

---

### 🗨️ **Postagem da Comunidade**
Usada na parte social da plataforma.

**Atributos:**
- id  
- usuario_id  
- conteudo  
- data  
- resposta  

**Métodos:**
- curtir()  
- editar()  
- deletar()  

---

## 🔗 Relacionamentos Importantes

- **Idioma 1..* → Curso**  
  Um idioma possui vários cursos.

- **Curso 1..* → Lição**  
  Cada curso contém várias lições.

- **Lição 1..* → Exercício**  
  Toda lição possui exercícios.

- **Usuário 1..* → Matrícula**  
  O usuário pode se matricular em diversos cursos.

- **Matrícula 1..* → Progresso**  
  Cada matrícula gera registros de progresso.

- **Usuário 1..* → Tentativa de Teste**  
  Cada tentativa registra pontuação e nível sugerido.

- **Usuário 1..* → Postagem Comunidade / Depoimento**  
  Representa interações sociais.

- **Teste de Nível 1..* → Tentativas**  
  Um teste pode ter várias tentativas feitas por diferentes usuários.

---

## 🖼️ Visualização do Diagrama


![Diagrama de Classe - Prime Language](https://github.com/user-attachments/assets/c278e594-9b6e-48e7-af2c-df304e39a9de)


