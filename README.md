# Victrl

Victrl is a focused fan control app for supported HP Victus laptops. Its first interface is a direct fan level slider with an Apply button and a Restore OEM Auto control.

## Current state

This initial version is adapted from [OmenCore](https://github.com/theantipopau/omencore), an MIT-licensed project. The direct fan control backend and hardware support database are retained; the fan screen is simplified for Victrl. The rest of the OmenCore app shell is still present in this first source snapshot.

This computer reports Victus board `8DD0`. OmenCore's model database includes that board and describes manual level writes, readback, and keepalive as supported. Hardware behavior still needs to be verified on the laptop after building.

## Build

On Windows with the .NET 10 SDK installed:

```powershell
dotnet build src/OmenCoreApp/OmenCoreApp.csproj -c Release
```

Run the app as administrator for HP firmware fan control. Use **Restore OEM Auto** to hand control back to the laptop firmware.

## License

This repository retains the upstream MIT license and notices. See [LICENSE](LICENSE) and the upstream [OmenCore repository](https://github.com/theantipopau/omencore).
