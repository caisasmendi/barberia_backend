# barberia_backend

## instalar dependendencias de postgres y entidades
dotnet add package Npgsql.EntityFrameworkCore.PostgreSQL
dotnet add package Microsoft.EntityFrameworkCore.Design

## herramienta para migraciones a bases de datos
dotnet tool install --global dotnet-ef

### para actualizar
dotnet tool update --global dotnet-ef

### cuando agregues o modifiques entidades 
dotnet ef migrations add InitialCreate
        aplica la migracion con : dotnet ef database update

### configurar coneccion a la base de datos 
 archivo: appsettings.json
 {
  "ConnectionStrings": {
    "DefaultConnection": "Host=localhost;Port=5432;Database=mi_base;Username=postgres;Password=tu_password"
  }
}