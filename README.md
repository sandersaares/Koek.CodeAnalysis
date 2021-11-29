# Koek.CodeAnalysis

Shared set of code analysis and code style settings.

# Usage

Prerequisites:

* You must be using a SDK-style project (the kind without `packages.config`).
* You must be using Visual Studio 2022 or newer.

Installation:

1. Install NuGet package `Koek.CodeAnalysis`.
1. Adjust the `PackageReference` and add the `GeneratePathProperty="true"` attribute.
1. Insert the below snippet into the `.csproj` file.

```xml
<PropertyGroup>
    <CodeAnalysisRuleset>$(PkgKoek_CodeAnalysis)\content\CodeAnalysis\CodeAnalysis.ruleset</CodeAnalysisRuleset>
</PropertyGroup>
```