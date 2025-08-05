# 🏰 Siegefend — C# Conversion

**Object‑Oriented Programming course project**  
_Created by Fabio Notaro_ (and team members: Bedei, Bertuccioli, Gessi)

This repository contains the **C# port of the “Siegefend” game** (originally in Java), following the course requirements. It includes classes and interfaces converted to .NET from the original **Siegefend** implementation, organized for easy compilation and extension.

## ⚙️ Project Overview

Siegefend is a turn‑based tower-defense game.

---

## 📋 Prerequisites

- Windows machine (or any OS supporting .NET 6 or .NET 7 SDK)
- **Visual Studio 2022+** or **Visual Studio Code** with C# extensions  
- [.NET SDK 6 or later](https://dotnet.microsoft.com/download) installed and `dotnet` available on your PATH


## 🏗️ Build & Run

### Visual Studio

1. Open `VS-Project\OOP21_task_cSharp.sln` in Visual Studio.
2. Restore NuGet packages (if prompted).
3. Set `Siegefend` as the startup project.
4. Run (Ctrl+F5) to see the console-based combat simulation. You can adjust battle parameters in `Program.cs`.

### .NET CLI (cross‑platform)

```bash
cd VS-Project/OOP21_task_cSharp
dotnet restore
dotnet build
dotnet run

Project Structure
/
├─ VS-Project/
│   └─ OOP21_task_cSharp/      ← Visual Studio solution & C# projects
│        ├─ Siegefend.csproj
│        ├─ Program.cs         ← main entry (sets up units & board)
│        ├─ Units\              ← Unit types & shared interfaces
│        ├─ Combat\             ← Battle logic, simulators, and effects
│        └─ Board\              ← Grid, placement logic, and round manager
├─ FabioNotaro2001/
│    └─ [Your converted classes—one folder per student in the original setup]
├─ .gitignore
├─ LICENSE (MIT)
└─ README.md (this file)
Each student (e.g. FabioNotaro2001, Bedei, etc.) may have added extended versions of units under their own folder; feel free to merge or refactor as needed.
🎯 How It Works

    Unit Creation – In Program.cs, you instantiate units (e.g. new MeleeUnit("Swordsman", 100, 15)).

    Placing Units – Units are placed on a Board (e.g. two opposing sides).

    Simulation – The BattleSimulator runs turn-based logic until one side is defeated or a draw occurs.

    Output – The console shows round-by-round actions and final winner.

You can customize behavior by subclassing a new unit type or modifying the strategy inside BattleSimulator.

Contributing

    If you add new unit types or strategy logic, please place your code in a properly named folder under ./VS-Project or ./FabioNotaro2001/.

    Ensure your code targets .NET 6 and passes a clean dotnet build.

📄 License

This project is licensed under the MIT License. See the LICENSE file for full terms.
Contact

Created by Fabio Notaro as part of the OOP course – feel free to raise an issue if you’d like enhancements, or contact via GitHub.

Enjoy diving into OOP design patterns using C#! 🚀
