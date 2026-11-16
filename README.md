# TinyShop

Starter solution for the GitHub Copilot workshop in Visual Studio 2026. The solution includes a .NET Aspire host, Minimal API product service, Blazor frontend, and tests.

## Start the workshop

```powershell
git clone https://github.com/jamesmontemagno/workshop-tinyshop.git
cd workshop-tinyshop
start src\TinyShop.sln
```

Open `src\TinyShop.sln` in Visual Studio 2026 and run **TinyShop.AppHost**.

`main` contains the intentionally incomplete starting point used by the workshop. To inspect the finished solution, switch to the `completed` branch:

```powershell
git switch completed
start src\TinyShop.sln
```

## Build

Install the .NET 10 or .NET 11 SDK, then run:

```powershell
dotnet build src\TinyShop.sln
```

The app targets .NET 10 and rolls forward to a newer major runtime if .NET 10 is not installed.

## License

MIT. The original workshop source and license are preserved from [dotnet-presentations/visual-studio-github-copilot-lab](https://github.com/dotnet-presentations/visual-studio-github-copilot-lab).
