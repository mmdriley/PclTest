# PclTest
`PclTest.sln` contains Portable Class Library projects targeting different PCL profiles. The solution also contains console applications targeting .NET 4.0 and .NET 4.5. These projects can be used to test how `TargetFrameworkProfile` and `TargetFrameworkVersion` affect the installation of NuGet packages.

## Included profiles

See also: [Stephen Cleary's _Framework Profiles in .NET_](http://blog.stephencleary.com/2012/05/framework-profiles-in-net.html)

|`TargetFrameworkProfile` |NuGet target framework moniker | .NET Standard |
|:-----------|:---|:---|
| Profile259 | `portable-net45+netcore45+wpa81+wp8` | `netstandard1.0` |
| Profile328 | `portable-net4+sl50+netcore45+wpa81+wp8` |
| Profile344 | `portable-net45+sl50+netcore45+wpa81+wp8` |

## Compatible PCL dependencies

Say `LibX` wants to depend on `LibY`, where both are PCLs. `LibY` must work *at least* everywhere `LibX` does. Otherwise, `LibX` would be claiming to target platforms on which it doesn't actually work. It's okay if `LibY` works in *more* places than `LibX`.
