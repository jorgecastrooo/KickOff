O **KickOff** é um sistema web desenvolvido em **Kotlin** com o framework **Ktor** no backend, utilizando **HTML, CSS e JavaScript** para o frontend e **MySQL** como base de dados. O objetivo principal é a gestão completa de uma plataforma de resultados desportivos, notícias, ligas, clubes e classificações.

## 📌 Índice
- [Introdução](#introdução)
- [Estrutura e Tecnologias](#estrutura-e-tecnologias)
- [Instalação e Configuração](#instalação-e-configuração)
- [Configuração do MySQL](#configuração-do-mysql)
- [Configuração da Base de Dados](#configuração-da-base-de-dados)
- [Como Iniciar o Projeto](#como-iniciar-o-projeto)
- [Funcionalidades](#funcionalidades)
- [Interface de Utilizador](#interface-de-utilizador)
- [Interface de Administração (ADM)](#interface-de-administração-adm)
- [Galeria do Projeto](#galeria-do-projeto)
- [Resolução de Problemas](#resolução-de-problemas)
- [Créditos](#créditos)

---

## 📝 Introdução
O sistema KickOff permite aos utilizadores acompanhar o mundo do futebol de forma simples e intuitiva. Oferece funcionalidades que vão desde o registo de utilizadores até à gestão avançada de jogos e estatísticas em tempo real para administradores.

---

## 🛠 Estrutura e Tecnologias
O projeto foi construído com as seguintes ferramentas:
* **Linguagem Principal:** Kotlin
* **Framework Backend:** Ktor
* **Frontend:** HTML5, CSS3, JavaScript
* **Base de Dados:** MySQL (v8.0.39)
* **Gestão de Dependências:** Gradle

![Estrutura de Pastas](6.png)

---

## ⚙️ Instalação e Configuração

### Configuração do MySQL
Antes de executar o projeto, é necessário instalar o MySQL Installer e o MySQL Workbench.
1. Descarregue o instalador em: [MySQL Downloads](https://dev.mysql.com/downloads/installer/).
2. Recomenda-se a versão **8.0.39**.

![Instalação MySQL](1.png)
![Workbench](2.png)

### Configuração da Base de Dados
1. No **MySQL Workbench**, crie uma conexão local.
2. Crie um schema chamado `kickoof`.
   *Nota: Se usar outro nome, altere o `jdbcUrl` no ficheiro `Application.kt`.*
3. Realize o **Data Import**:
    - Vá a `Server > Data Import`.
    - Selecione "Import from Self-Contained File" e aponte para o ficheiro `BD_kotlin`.
    - Escolha o schema de destino e clique em **Start Import**.

![Importação](5.png)

---

## 🚀 Como Iniciar o Projeto
1. Abra o projeto no **IntelliJ IDEA**.
2. Navegue até `src/main/kotlin/Application.kt`.
3. Configure a sua password da base de dados na variável `password`.
4. Execute o projeto.
5. No navegador, aceda a: `http://localhost:8082/static/index.html`.

---

## ✨ Funcionalidades

### Interface de Utilizador
* **Login e Registo:** Sistema com validação de idade mínima (13 anos) e encriptação de dados.
* **Homepage:** Acesso rápido a notícias e menus de navegação.
* **Resultados:** Consulta de jogos passados e futuros com filtros de data.
* **Classificações:** Tabela dinâmica com vitórias, derrotas, empates e saldo de golos.
* **Notícias:** Feed organizado por categorias como "Transferências".

### Interface de Administração (ADM)
*Acesso:* `Username: jorge_2` / `Password: J0rgec@stro`.
* **Gerir Resultados:** Edição de golos, cartões e finalização de jogos com atualização automática de estatísticas.
* **Gerir Utilizadores:** Pesquisa, remoção de contas e promoção de utilizadores a administradores.
* **Gestão de Conteúdos:** Criação, edição e eliminação de equipas, ligas, notícias e jogos.

---

## 🖼 Galeria do Projeto

### Acesso e Registo
![Login](8.png)
![Registo](9.png)

### Visualização de Dados
![Home](10.png)
![Resultados](11.png)
![Classificação](12.png)

### Painel Administrativo
![Gestão Utilizadores](17.png)
![Gestão Equipas](19.png)
![Gestão Jogos](21.png)

---

## ⚠️ Resolução de Problemas
* **Erro no Build (test):** Pode ocorrer um erro durante os testes automatizados. Este erro pode ser ignorado, pois não impede a execução do projeto.
* **Erro SLF4J:** Ao iniciar, pode surgir um aviso sobre o SLF4J não ser encontrado. Se a aplicação conectar à base de dados, ignore a mensagem.

---

## 👥 Créditos
Projeto desenvolvido por:
* **Afonso Martins** - nº 2024168
* **Jorge Castro** - nº 2024454
* **Turma:** A DDM

![ISTEC](22.png)
