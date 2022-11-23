# _Entity Framework_ - _Cheatsheet_ (cola)

Crie seu banco de dados normalmente. Anote as seguintes informações:

- Endereço do servidor (se for seu computador local, é `localhost`);
- Porta do servidor (a padrão é `3306`);
- As credenciais de acesso: usuário e senha (na Etec usa-se por padrão usuário `root` e senha `12345`);
- - O nome do banco de dados (usado no `CREATE DATABASE`).

## Instalação do _Entity Framework Core .NET Command-line Tools_

Verifique se já está instalado usendo no terminal (caso esteja instalado, aparecerá o número da versão):
```
dotnet ef --version
```

Se não estiver, instale globalmente usando:
```
dotnet tool install --global dotnet-ef
```

Se estiver instalada, atualize usando:
```
dotnet tool update --global dotnet-ef
```

## Criando o projeto

Crie o seu projeto normalmente, usando o template desejado:
- `dotnet new console` para projetos console, ou
- `dotnet new webapi` para backend web.

## Instalando as dependências

Precisamos instalar todas as bibliotecas que serão usadas no projeto, usando o Nuget.

Instale o _Entity Framework_ no projeto:
```
dotnet add package Microsoft.EntityFrameworkCore
dotnet add package Microsoft.EntityFrameworkCore.Design
```

Instale o _driver_ para MySQL _Pomelo_ no projeto:
```
dotnet add package Pomelo.EntityFrameworkCore.MySql
```

## Criando a _string de conexão_

Crie a sua _string de conexão_ e mantenha anotada em algum local. Para isso, substitua as lacunas `___` pelos valores identificados no início deste material.

```
server=___;port=___;user=___;password=___;database=___
```

- `server` indica o endereço do servidor (ex. `localhost`);
- `port` indica a porta do servidor (ex. `3306`);
- `user` indica o usuário (ex. `root`);
- `password` indica a senha (ex. `12345`);
- `database` indica o nome do banco de dados (ex. `agenda`).

Nesse exemplo, a _string de conexão_ seria:
```
server=localhost;port=3306;user=root;password=12345;database=agenda
```

## Fazendo o _scaffolding_

Para criar automaticamente as classes necessárias para representar nosso banco de dados, substitua a lacuna `___` pela sua string de conexão e execute:
```
dotnet ef dbcontext scaffold "___" Pomelo.EntityFrameworkCore.MySql -o db -f --no-pluralize
```

As classes serão criadas na pasta `db` (indicada no parâmetro `-o pasta`).
