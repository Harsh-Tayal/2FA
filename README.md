# Two-Factor Authentication with Microsoft Authentication in C#

# Overview

This project illustrates the implementation of two-factor authentication (2FA) using Microsoft Authentication in a C# application. 2FA enhances security by requiring users to provide a second form of authentication, usually a code sent to their registered device, in addition to their username and password.

# Prerequisites

- .NET Core or .NET Framework
- Visual Studio or another C# IDE

# Setup to Implement 2FA

```bash
git clone https://github.com/Harsh-Tayal/2FA.git
```

## 1 Choose 2FA Method

Decide which method(s) of 2FA you want to support. Common methods include SMS, email, authenticator apps, or hardware tokens.

## 2. Add Required Packages:

Ensure that the following NuGet packages are installed in your ASP.NET Core project:

- **Microsoft.AspNetCore.All**: This package includes a set of core libraries for ASP.NET Core applications.
- **Microsoft.EntityFrameworkCore**.Tools: This package provides Entity Framework Core tools for migrations and database management.
- **Microsoft.NETCore.App**: This package contains the .NET Core runtime and library.
- **Microsoft.VisualStudio.Web.CodeGeneration.Design**: This package provides design-time support for scaffolding controllers and views in Visual Studio.

## 3 Connection String:

```bash
"ConnectionStrings": {
    "DefaultConnection": "Server=your_server;Database=your_database;User=your_username;Password=your_password;"
}
```

## 4 Update Identity Configuration:

If using ASP.NET Core Identity, configure it to support 2FA. This may involve enabling 2FA options in Identity settings.

## 5 Generate and Verify Codes:

Implement logic to generate and verify 2FA codes for the chosen method(s). This typically involves generating a random code, sending it to the user via the selected method, and then verifying the code when the user submits it.

## 6 UI Changes

Modify the user interface to accommodate the 2FA flow. Add an additional step in the login process where the user enters their 2FA code.

## 7 Enforce 2FA

Decide when and where to enforce 2FA. You may require 2FA for certain sensitive actions, such as changing account settings or accessing sensitive data.

### Technologies Used

- C#
- ASP.NET Core
- Entity Framework Core
- SQL Server
