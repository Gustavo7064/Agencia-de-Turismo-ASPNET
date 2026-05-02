# ✈️ Agência de Turismo ASP.NET

Sistema web de agência de turismo desenvolvido em ASP.NET Core MVC com banco de dados MySQL. Permite o gerenciamento de destinos, pacotes de viagem, clientes e reservas, com autenticação e controle de acesso por perfil.

---

## 🚀 Tecnologias Utilizadas

- **ASP.NET Core MVC** — framework web principal
- **C#** — linguagem de programação
- **MySQL** — banco de dados relacional
- **MySql.Data** — conector MySQL para .NET
- **Bootstrap** — estilização do frontend
- **HTML/CSS/Razor** — frontend das views

---

## ⚙️ Funcionalidades

- 🌍 Cadastro e listagem de destinos turísticos
- 📦 Gerenciamento de pacotes de viagem (tipo, duração, preço, vagas)
- 👤 Cadastro de clientes com CPF, e-mail e data de nascimento
- 📅 Controle de reservas com status e valor total
- 🔐 Autenticação de usuários com controle de acesso por perfil
- 🛠️ Painel administrativo

---

## 🗄️ Banco de Dados

O projeto utiliza **MySQL**. O script de criação do banco está em `projectPartiuDestino/database/schema.sql`.

**Tabelas principais:**
- `usuarios` — usuários do sistema com roles e controle de acesso
- `destinos` — destinos disponíveis com país e descrição
- `pacotes` — pacotes de viagem vinculados a destinos
- `clientes` — clientes cadastrados vinculados a usuários
- `reservas` — reservas de pacotes feitas pelos clientes

---

## 🛠️ Como Rodar o Projeto

### Pré-requisitos

- [.NET SDK 6.0+](https://dotnet.microsoft.com/download)
- [MySQL Server](https://dev.mysql.com/downloads/)
- [Visual Studio 2022](https://visualstudio.microsoft.com/) ou VS Code

### Passo a passo

1. **Clone o repositório**

git clone https://github.com/seu-usuario/Agencia-de-Turismo-ASPNET.git
cd Agencia-de-Turismo-ASPNET

2. **Configure o banco de dados**
   - Abra o MySQL e execute o script: `source projectPartiuDestino/database/schema.sql;`

3. **Configure a string de conexão**
   - Em `projectPartiuDestino/Data/Conexao.cs`, ajuste com seu usuário e senha do MySQL.

4. **Rode o projeto**

cd projectPartiuDestino
dotnet run

Ou abra a solution `projectPartiuDestino.sln` no Visual Studio e pressione `F5`.

---

## 📁 Estrutura do Projeto

Agencia-de-Turismo-ASPNET/
└── partiuDestino/
    ├── projectPartiuDestino.sln
    └── projectPartiuDestino/
        ├── Controllers/        # Rotas: Home, Login, Cadastro, Admin, Personalizada
        ├── Data/               # Conexão com o banco de dados
        ├── Models/             # Classes de modelo (Usuario...)
        ├── Views/              # Páginas Razor (.cshtml)
        ├── wwwroot/            # CSS, JS e imagens estáticas
        ├── database/           # Script SQL do banco
        └── Program.cs          # Configuração da aplicação

---

## 👥 Perfis de Acesso

| Perfil  | Permissões                        |
|---------|-----------------------------------|
| Admin   | Acesso total ao painel            |
| User    | Consulta de pacotes e reservas    |

---

## 📄 Licença

Este projeto foi desenvolvido para fins educacionais.
