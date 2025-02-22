# StrAnalyticsOpen

## 📖 Sobre o Projeto

O **StrAnalyticsOpen** é um sistema de controle de vendas e serviços para a loja STR Ar Condicionados. Este projeto foi desenvolvido para fornecer uma plataforma onde a loja pode gerenciar suas vendas e serviços de maneira eficiente.

## 🌟 Funcionalidades Principais

- **Gestão de Produtos:**
  - Listagem, criação, edição e exclusão de produtos.
  
- **Gestão de Vendas:**
  - Registro de vendas com detalhes dos produtos vendidos.
  - Consulta de vendas com filtros de data e valores.
  
- **Gestão de Serviços:**
  - Registro de serviços prestados com detalhes dos clientes e serviços realizados.
  - Consulta de serviços com filtros de data e categorias.

## 🔧 Tecnologias Utilizadas

- **Backend:**
  - C#
  - ASP.NET Core MVC
  
- **Banco de Dados:**
  - SQL Server (Entity Framework Core como ORM)
  
- **Frontend:**
  - Razor Pages
  - HTML/CSS/Bootstrap

## 📂 Estrutura do Projeto

```plaintext
StrAnalyticsOpen/
├── Controllers/
│   ├── ProductsController.cs
│   ├── SalesController.cs
│   └── ServicesController.cs
├── Models/
│   ├── Product.cs
│   ├── Sale.cs
│   └── Service.cs
├── Data/
│   ├── SeedingService.cs
│   └── StrAnalyticsOpenContext.cs
├── Views/
│   ├── Products/
│   ├── Sales/
│   └── Services/
└── wwwroot/
```

### Pastas Principais:
- **Controllers:** Contém a lógica de controle de rotas e ações da aplicação.
- **Models:** Contém as classes que representam as entidades do sistema.
- **Views:** Contém as páginas da aplicação renderizadas para o usuário.
- **Data:** Contém a configuração do banco de dados e o serviço de preenchimento inicial de dados.

## 🖥️ Configuração e Execução

### Pré-requisitos

- .NET SDK 7.0 ou superior.
- SQL Server configurado.
- Visual Studio ou VS Code.

### Passo a Passo

1. Clone o repositório:
    ```bash
    git clone https://github.com/GuilhermeBomfimDev/StrAnalyticsOpen.git
    ```

2. Navegue até a pasta do projeto:
    ```bash
    cd StrAnalyticsOpen
    ```

3. Configure a conexão com o banco de dados no arquivo `appsettings.json`. OBS: Utilize apenas uma String por vez (Local ou Hospedada):
    ```json
    "ConnectionStrings": {
      "StrAnalyticsContext":
      /*String de conexão com o banco de dados hospedado no Azure*/
      "Server=tcp:{Nome-do-seu-server}.database.windows.net,1433;Initial Catalog=stranalytics;Persist Security Info=False;User ID={Seu-IdName};Password={Sua-  Senha};MultipleActiveResultSets=False;Encrypt=True;TrustServerCertificate=False;Connection Timeout=30;"
      
      /*String de conexão com o banco de dados local*/
      "Server=localhost\\SQLEXPRESS;Database=stranalytics;User Id=sa;Password={Sua-Senha};TrustServerCertificate=True;"
    }
    ```
  
4. Crie uma migration se necessárioo:
    ```Nugget Package Console
    Add-Migration {Nome-da-Migration}
    ```
    
5. Execute as migrações para criar o banco de dados:
    ```Nugget Package Console
    Update-Database
    ```
    OU
    ```bash
    dotnet ef database update
    ```

7. Execute o projeto:
    ```bash
    dotnet run
    ```

8. Acesse o sistema no navegador em:
    ```plaintext
    https://localhost:5001
    ```

## 🤝 Contribuições

Contribuições são bem-vindas! Sinta-se à vontade para abrir uma issue ou enviar um pull request com melhorias e novas funcionalidades.

## 📜 Licença

Este projeto é licenciado sob a [MIT License](LICENSE).

---

Feito por Guilherme Bomfim.
# StrAnalyticsOpen
