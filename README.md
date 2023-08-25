# Prog-II-Atividade

1- Crie um projeto ASP.NET MVS (template) com nome PjNomeSobrenome
2- Configure no projeto os NuGet Packages do EF Core
3- Especifique uma classe Model para Psicologo e defina um DbContext
	herdando do Identity
4- Configure no appsettings.json uma string de conexão com o SQL Server
5- Defina os parâmetros de configuração dos serviços da aplicação no program.cs
5- Crie a migration (dotnet ef migrations add Initial) e atualiza o banco (dotnet ef database update)

Roteiro:

Criar um projeto com o Visual Studio > Utilizar o modelo de projeto "Aplicativo Web do ASP.NET Core (MVC)
	> Renomear o projeto > Selecionar a versão do .net e desativar o HTTPS

Abrir o gerenciador dos pacotes NuGet e instalar os pacotes:
	> Microsoft.AspNetCore.Identity.EntityFrameworkCore
	> Microsoft.EntityFrameworkCore.Design
	> Microsoft.EntityFrameworkCore.SqlServer

Na pasta Models criar dois novos itens de Classe C#, "AppUser" e "Psicologo"; 
	> Em AppUser definimos os objetos que todos os tipos de cadastros usarão (Um perfil de usuário geral)
	> Na classe Psicologo, definimos os objetos específicos para a classe (Id, Name, Crmv, Liberate) e herdamos os objetos de AppUser; 
	> Definir chave primária, chave estrangeira, mensagens de erro e requisições.

Criamos uma pasta Data e dentro dela, uma classe e definimos o BdContext herdando do Identity

Em appsettings.json criamos um usuário para o Admin e setamos uma string para a conexão

Em Program.cs adicionamos as obrigatoriedades e requisições para criação de usuário e senha

Dentro da pasta do projeto instalamos o EF utilizando "dotnet tool install --global dotnet-ef"
	> criar a Migration utilizando "dotnet ef migrations add Initial"
	> Ainda dentro da pasta, atualizamos o banco de dados utilizando "dotnet ef database update"
