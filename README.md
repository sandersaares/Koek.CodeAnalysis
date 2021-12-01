# Koek.CodeAnalysis

Shared set of code analysis and code style settings.

# Usage

Prerequisites:

* You must be using a SDK-style project (the kind without `packages.config`).
* You must be using Visual Studio 2022 or newer.

Installation:

1. Install NuGet package `Koek.CodeAnalysis`.
1. Insert the below property into the `.csproj` file.

```xml
<CodeAnalysisRuleset>$(PkgKoek_CodeAnalysis)\content\CodeAnalysis.ruleset</CodeAnalysisRuleset>
```

The last step must be performed manually, as you may wish to customize when the ruleset is applied and/or merge it to another ruleset.

To actually enable code analysis, you may want to define the following properties:

```xml
<EnforceCodeStyleInBuild>True</EnforceCodeStyleInBuild>
<EnableNETAnalyzers>True</EnableNETAnalyzers>
<AnalysisLevel>preview</AnalysisLevel>
```