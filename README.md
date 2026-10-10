# safe-exam-c

Requires Windows, .NET 8 and the WebView2 runtime. This environment has no dotnet/Windows UI, so the new CI job has not run here. Verify lockdown, exit, reconnect and fail/recovery behavior on real Windows before claiming anti-cheat enforcement.

## Verification

```sh
On Windows: dotnet test native-client/src/SafeExam.Tests/SafeExam.Tests.csproj -c Release
```

[Audit fixes and limits](AUDIT_FIXES.md).
