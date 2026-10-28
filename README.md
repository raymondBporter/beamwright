# Beamwright desktop

This solution references `App2d.Core` from an existing App2d checkout. It does not contain a copy of Core.

Requires Windows and the .NET 10 SDK. By default, place this repository beside the `App2d` checkout:

```text
source/
  App2d/
    App2d.Core/
  beamwright-dotnet/
    Beamwright.slnx
```

```powershell
dotnet build Beamwright.slnx
dotnet test App2d.Beamwright.Tests
dotnet run --project App2d.Beamwright
```

For another checkout location, add `-p:App2dRoot=C:/path/to/App2d` to these commands. Core's NuGet packages and build analyzers are restored from that checkout.

Campaign notes, controls, verification and attribution: [desktop notes](App2d.Beamwright/README.md). The imported content license and third-party notices remain with the application.

Verify all campaign solutions with `dotnet run --project App2d.Beamwright -- --verify`.
