# Native verification entry point

Repair branch: `fix/internship-audit-20261010`. Changes are scoped to audit findings; no deployment or live provider action is included.

## Changed

Added missing repository-level setup documentation and Windows .NET 8 test CI. No Linux-only workaround was substituted for WPF/WebView2 behavior.

## Verification

`On Windows: dotnet test native-client/src/SafeExam.Tests/SafeExam.Tests.csproj -c Release`

Commands are entry points, not a claim that every live integration was executed. See the repair bundle for actual results.

## Setup and remaining evidence

Requires Windows, .NET 8 and the WebView2 runtime. This environment has no dotnet/Windows UI, so the new CI job has not run here. Verify lockdown, exit, reconnect and fail/recovery behavior on real Windows before claiming anti-cheat enforcement.
