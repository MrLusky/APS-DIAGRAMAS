# 🗂️ Diagrama de Atividades — Prime Language

Este diagrama representa o **fluxo de atividades do aluno** dentro do **site e aplicativo da escola de idiomas _Prime Language_**.  
Ele descreve de forma visual como o usuário interage com o sistema e como essas ações se conectam com o **banco de dados**.

---

## 🎯 Objetivo do Diagrama

O objetivo deste diagrama é **demonstrar o funcionamento geral do sistema do ponto de vista do aluno**, mostrando o percurso das ações mais comuns dentro da plataforma.  
Ele serve como uma **ferramenta de entendimento e documentação** para desenvolvedores, analistas e demais envolvidos no projeto.

O diagrama aborda:
- O processo de **login e autenticação** do aluno.  
- O **acesso a cursos, aulas e atividades**.  
- A **interação com a comunidade** (amigos, conversas e mensagens).  
- A **gestão do perfil do usuário** (edição, exclusão e atualização de dados).  
- O **encerramento da sessão** (logout).  

---

## 🧩 Partes do Sistema Representadas

| Camada | Responsável | Funções principais |
|:--|:--|:--|
| **Aluno (Usuário)** | Interage com o sistema | Realiza login, acessa cursos, gerencia perfil e participa da comunidade. |
| **Site/App (Interface)** | Executa ações de interface | Exibe páginas, processa interações e envia requisições ao servidor. |
| **Banco de Dados (Back-end)** | Armazena e valida informações | Autentica usuários, salva alterações, gerencia dados e registros. |

---

## 🔄 Fluxo Geral

1. O aluno entra no site/app e insere seu e-mail e senha.  
2. O sistema valida o login com o banco de dados.  
3. Após o acesso autorizado, o aluno pode:  
   - Visualizar e acessar cursos e aulas.  
   - Jogar *WordGuess* e realizar atividades.  
   - Alterar dados de perfil ou deletar a conta.  
   - Participar da comunidade (adicionar amigos, enviar mensagens).  
4. Todas as alterações e interações são **salvas ou validadas no banco de dados**.  
5. Por fim, o aluno pode **fazer logout**, encerrando sua sessão.

---

## 🖼️ Visualização do Diagrama

![Prime Language](https://github.com/user-attachments/assets/5efa91d5-77ae-438a-9387-a4ab8fcb4ed1)



