```markdown
# CrudDotNet

## Description

CrudDotNet is an ASP.NET Core 8.0 MVC project with a SQL Server 2014 database. This project demonstrates basic CRUD operations on a `Category` model, including the use of SweetAlert2 for delete confirmation dialogs.

## Features

- Create, Read, Update, and Delete (CRUD) operations on categories.
- SweetAlert2 integration for confirmation dialogs.
- Uses Entity Framework Core for database access.

## Prerequisites

Before you begin, ensure you have met the following requirements:

- **.NET SDK 8.0**: Download and install from [Microsoft .NET](https://dotnet.microsoft.com/download/dotnet/8.0).
- **SQL Server**: Ensure you have SQL Server 2014 or later installed.
- **Node.js and npm**: Download and install from [Node.js](https://nodejs.org/) (for managing frontend dependencies like SweetAlert2).

## Installation

Follow these steps to set up the project locally:

1. **Clone the repository**:
   ```bash
   git clone https://github.com/USERNAME/REPOSITORY.git
   cd REPOSITORY
   ```

2. **Set up the database connection**:
   - Open `appsettings.json` and update the `ConnectionStrings` section with your SQL Server details:
     ```json
     {
       "ConnectionStrings": {
         "AvisEntities": "Server=YOUR_SERVER;Database=YOUR_DATABASE;Trusted_Connection=True;TrustServerCertificate=True;"
       }
     }
     ```

3. **Restore the .NET dependencies**:
   ```bash
   dotnet restore
   ```

4. **Install the required tools**:
   ```bash
   dotnet tool install --global dotnet-ef
   ```

5. **Add the Entity Framework Core Design package**:
   - Open your `.csproj` file and ensure the following package reference is included:
     ```xml
     <ItemGroup>
       <PackageReference Include="Microsoft.EntityFrameworkCore.Design" Version="8.0.6" />
     </ItemGroup>
     ```

6. **Apply migrations and update the database**:
   ```bash
   dotnet ef migrations add InitialCreate
   dotnet ef database update
   ```

7. **Install SweetAlert2 via npm**:
   - If npm is not installed, follow the installation instructions from the Node.js website.
   - Once npm is installed, run:
     ```bash
     npm install sweetalert2
     ```

8. **Run the application**:
   ```bash
   dotnet run
   ```

## Usage

Once the application is running, you can:

- Navigate to `https://localhost:5001` to access the web application.
- Use the UI to perform CRUD operations on categories.

## Contributing

If you wish to contribute to this project, please follow these steps:

1. Fork the repository.
2. Create a new branch:
   ```bash
   git checkout -b feature-branch
   ```
3. Make your changes and commit them:
   ```bash
   git commit -m "Description of changes"
   ```
4. Push to the branch:
   ```bash
   git push origin feature-branch
   ```
5. Create a pull request.

## License

This project is licensed under the MIT License. See the `LICENSE` file for more information.

## Contact

If you have any questions or feedback, please open an issue or contact [Anis Rahmani](mailto:arahmani@kaiteck.com).
```
