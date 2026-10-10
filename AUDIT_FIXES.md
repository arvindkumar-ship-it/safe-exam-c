# Native verification entry point

Repair branch: `fix/internship-audit-20261010`. Changes are scoped to audit findings; no deployment or live provider action is included.

## Changed

Added missing repository-level setup documentation and a Windows .NET 8 CI entry point. Added explicit System.IO and System.Net.Http imports after the first CI run exposed missing namespaces.

## Verification

`On Windows: dotnet test native-client/src/SafeExam.Tests/SafeExam.Tests.csproj -c Release`

Commands are entry points, not a claim that every live integration was executed. See the repair bundle for actual results.

## Setup and remaining evidence

Requires Windows, .NET 8 and the WebView2 runtime. The Windows CI rerun still fails compilation: the configured SafeExam.Client.Program startup class is absent, and BrowserHost uses a CoreWebView2Controller property unavailable on the WPF control. The test project contains no test source files. The PR remains draft pending native startup/controller repair and actual tests. Verify lockdown, exit, reconnect and fail/recovery behavior on real Windows before claiming anti-cheat enforcement.
