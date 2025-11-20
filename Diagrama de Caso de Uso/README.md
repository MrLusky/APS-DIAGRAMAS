# 🗂️ Diagrama de Caso de Uso — Prime Language

Este diagrama representa **as funcionalidades principais oferecidas pelo sistema Prime Language**, mostrando como **Usuários** e **Administradores** interagem com as diversas ações permitidas dentro da plataforma.

Ele descreve *o que* o sistema oferece — isto é, seus **casos de uso** — sem detalhar *como* eles são realizados.

---

## 🎯 Objetivo do Diagrama

O objetivo deste diagrama é **documentar e explicar o conjunto de funcionalidades disponíveis**, além de mostrar:

* Quem são os **atores** que utilizam o sistema.
* Quais **ações** cada tipo de usuário pode executar.
* As relações de dependência entre funcionalidades por meio de

  * `<<include>>` (função necessária)
  * `<<extend>>` (função opcional/complementar).

Esse diagrama serve como referência para desenvolvedores, analistas e qualquer membro da equipe que precise entender **as responsabilidades de cada ator** dentro do sistema.

---

## 🧩 Partes do Sistema Representadas

| Elemento                            | Descrição                                                                                                                      |
| ----------------------------------- | ------------------------------------------------------------------------------------------------------------------------------ |
| **Usuário**                         | Pessoa que utiliza o app/site para aprender idiomas, interagir com a comunidade e realizar atividades.                         |
| **Admin**                           | Responsável pela administração da plataforma, manutenção de atividades e gerenciamento do progresso e recompensas de usuários. |
| **Casos de Uso**                    | Funcionalidades acessíveis pelos atores (ex.: criar usuário, realizar atividades, recompensar usuário, etc.)                   |
| **Relações (`include` / `extend`)** | Indicam quando uma ação depende de outra ou quando é uma extensão opcional.                                                    |

---

## 🔄 Funcionalidades Principais

### 👤 **Ações do Usuário**

O usuário pode:

* Criar conta
* Iniciar sessão
* Recuperar senha (`extend` de iniciar sessão)
* Editar seu usuário (`include` iniciar sessão)
* Interagir com a comunidade
* Realizar atividades (`include` iniciar sessão)
* Adicionar idioma

  * Pode realizar **teste de proficiência** (`extend`)

Essas funções mostram o fluxo natural de um aluno dentro da plataforma: criar login → entrar → usar recursos → ajustar perfil → realizar atividades.

---

### 🛠️ **Ações do Administrador**

O Admin tem papel de manutenção e supervisão:

* **Manter atividades** (criar, editar, remover)
* **Recompensar usuários** (ex.: XP, conquistas, bônus)
* **Manter a “Streak”** dos usuários

Essas ações garantem o bom funcionamento da plataforma e o engajamento dos usuários.

---

## 🔗 Relações Importantes no Diagrama

* **`<<include>>`**: indica que um caso *sempre depende* de outro para acontecer.
  Exemplo:

  * Editar usuário **inclui** iniciar sessão → só edita se estiver logado.
  * Realizar atividades **inclui** iniciar sessão.

* **`<<extend>>`**: indica que a funcionalidade é complementar/opcional.
  Exemplo:

  * Recuperar senha **estende** iniciar sessão → só ocorre se o login falhar.
  * Teste de proficiência **estende** adicionar idioma.

---

## 🖼️ Visualização do Diagrama

![Caso de Uso](https://github.com/user-attachments/assets/a6ea3ab9-ac09-4b24-beaf-c99d419d669e)


