# SARIF
The **Static Analysis Results Interchange Format** (**SARIF**; pronunciation_guide) is a universal representation for the output of [static analysis](https://en.wikipedia.org/wiki/Static_analysis) tools.  It is standardized by the [OASIS](https://en.wikipedia.org/wiki/OASIS_(organization)) [SARIF Technical Committee](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=sarif).

### Contents
1. Purpose
2. Standard
3. History
4. Adoption
5. See also
6. References

## Purpose
SARIF creates one common format for representing the results of static analysis tools. This allows visualization tools to work with static analysis tools from multiple vendors. It also facilitates the aggregation of static analysis output from the tools of multiple vendors.

Each static analysis tool has a unique approach to discovering properties of computer program source code. Consequently, tools from different vendors find different sets of vulnerabilities. Combining the output of tools from multiple vendors can provide a more complete picture of vulnerabilities in source code.

By supporting SARIF, a low-cost tool provider gets access to a rich ecosystem of support.

## Standard
The current version of the standard, v2.1.0, is [publicly available from OASIS](https://docs.oasis-open.org/sarif/sarif/v2.1.0/sarif-v2.1.0.html).

### How SARIF relates to other standards

(to be completed)

(possibly include a mention of [STIX](https://www.mitre.org/sites/default/files/publications/stix.pdf))

## History
Early work on SARIF began within Microsoft for use in their tools. It eventually became apparent that SARIF's value could be substantially enhanced by making it an industry-wide standard.

The OASIS SARIF Technical Committee was formed and had its first meeting in September, 2017. The first edition of the SARIF standard was published in March, 2020. It was called version 2.1.0 in recognition of the earlier efforts within Microsoft as well as intermediate pre-standard versions that were in use during the development of the standard. Following publication, the committee suspended its activities, resuming beginning in March, 2021, to begin discussing the direction for future editions of the standard.

## Adoption

### Direct support

- [BinSkim](https://github.com/microsoft/binskim) is a binary-level security checker that validates Window, Mac and *nix binaries.
- [Brakeman](https://github.com/presidentbeef/brakeman/) is a static analysis tool which checks Ruby on Rails applications for security vulnerabilities.
- [Checkstyle](https://github.com/checkstyle/checkstyle) is a Java style guidelines checking.
- [Clang Analyzer](https://clang-analyzer.llvm.org/), the LLVM C/C++ checker, has [added SARIF export](https://github.com/llvm-mirror/clang/commit/962c092aae53360ab4d5b1adac78963694b5963f).
- [CodeQL](https://github.com/github/codeql) is a multilanguage, intraprocedural checker with a large rule set.
- [CodeSonar](https://www.grammatech.com/codesonar-cc) is a static analysis tool which identifies programming bugs that can result in system crashes, memory corruption, leaks, data races, and security vulnerabilities.
- [CredScan](https://secdevtools.azurewebsites.net/helpcredscan.html) is a file scanner that detects plaintext secrets.
- [DartAnalyzer](https://github.com/dart-lang/sdk/tree/master/pkg/analyzer_cli#dartanalyzer) is a dart/flutter analyzer.
- [Detekt](https://github.com/detekt/detekt) is a static code analysis tool for the Kotlin programming language.
- [DevSkim](https://github.com/microsoft/devskim) is a set of IDE checkers and language analyzers that provide inline security analysis.
- [Electronegativity](https://github.com/doyensec/electronegativity) is a tool to identify misconfigurations and security anti-patterns in Electron-based applications.
- [ESLint Sarif Formatter](https://www.npmjs.com/package/eslint.formatter.sarif) enables SARIF export for [ESLint](https://eslint.org/), a JavaScript static analyzer.
- [Flawfinder](https://github.com/david-a-wheeler/flawfinder) is a C/C++ source code security checker.
- [FortifyVulnerabilityExporter](https://github.com/fortify/FortifyVulnerabilityExporter#github-configuration) allows exporting vulnerabilities from Fortify on Demand and Fortify Software Security Center to third-party products and output formats.
- [Fortify Ssc Parser](https://github.com/fortify-ps/fortify-ssc-parser-sarif) is a plugin allows for importing SARIF (Static Analysis Results Interchange Format) files.
- [GoSec](https://github.com/securego/gosec) is a GoLang security checker.
- [Kubesec](https://github.com/controlplaneio/kubesec), backed by ControlPlane.io provides Security risk analysis for Kubernetes resources.
- [MobSF](https://github.com/MobSF/Mobile-Security-Framework-MobSF) is is an automated, all-in-one mobile application (Android/iOS/Windows) pen-testing, malware analysis and security assessment framework capable of performing static and dynamic analysis.
- [NodeJSScan](https://github.com/ajinabraham/nodejsscan) is a Static security code scanner (SAST) for Node.js applications.
- [Psalm](https://github.com/vimeo/psalm) is an open source tool for finding security vulnerabilities in PHP.
- [PMD](https://github.com/pmd/pmd/issues/2953) is a multilanguage source code analyzer.
- [PSScriptAnalyzer](https://github.com/PowerShell/PSScriptAnalyzer) is a static code checker for PowerShell modules and scripts
- [PREfast](https://docs.microsoft.com/cpp/build/reference/analyze-code-analysis?view=msvc-160) is the C/C++ correctness checker behind the Microsoft compiler /analyze switch.
- [Roslyn](https://github.com/dotnet/roslyn-analyzers) is a platform for analyzing and rewriting C#/VB.NET code.
- [SARIF Pattern Matcher](https://github.com/microsoft/sarif-pattern-matcher) is a security-focused pattern matcher that detects (and in some cases authenticates) plaintext secrets, sensitive data, etc.
- [Security Code Scan](https://github.com/security-code-scan/security-code-scan) is a Vulnerability Patterns Detector for C# and VB.NET.
- [Semgrep](https://github.com/returntocorp/semgrep), sponsored by [R2C](https://r2c.dev/), supports a [variety of languages](https://semgrep.dev/docs/status/).
- [Sobelow](https://github.com/nccgroup/sobelow) is the security-focused static analyzer for the Elixir Phoenix Framework.
- [SpotBugs](https://github.com/spotbugs/spotbugs) is a Java code checker.
- [TFSec](https://github.com/tfsec/tfsec) uses static analysis of your terraform templates to spot potential security issues.
- [Trivy](https://github.com/aquasecurity/trivy) is a vulnerability scanner for containers and other artifacts.

### Converters (i.e. tool output to SARIF conversion code exists)

- AndroidStudio
- Bandit
- CppCheck
- ContrastSecurity
- Fortify
- FortifyFpr
- FxCop
- Pylint
- StaticDriverVerifier
- TSLint

### SDKs/Documentation

- [C#](https://github.com/microsoft/sarif-sdk)
- [JS](https://github.com/microsoft/sarif-js-sdk)
- [Python](https://github.com/microsoft/sarif-python-om)
- [Go](https://github.com/owenrumney/go-sarif)
- [SARIF Tutorials](https://github.com/microsoft/sarif-tutorials)

### Viewers/SARIF development Support

- [Visual Studio Extension](https://github.com/microsoft/sarif-visualstudio-extension)
- [Visual Studio Code](https://github.com/microsoft/sarif-vscode-extension)
- [AzureDevops Extension](https://github.com/microsoft/sarif-azuredevops-extension)
- [SARIF Viewer](https://microsoft.github.io/sarif-web-component/)
- [SARIF Validator](https://sarifweb.azurewebsites.net/)
- [GitHub docs](https://docs.github.com/en/enterprise-server@3.0/code-security/secure-coding/integrating-with-code-scanning/sarif-support-for-code-scanning#about-sarif-support)

## See also

* [Static analysis](https://en.wikipedia.org/wiki/Static_analysis)

## References
