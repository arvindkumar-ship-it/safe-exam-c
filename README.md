# safe-exam-c

Requires Windows, .NET 8 and the WebView2 runtime. Windows CI currently fails compilation: the configured `SafeExam.Client.Program` startup class is missing and `BrowserHost` references a `CoreWebView2Controller` property unavailable on the WPF control. The test project currently contains no test source files. Resolve these blockers and add native tests before treating this command as verification. Verify lockdown, exit, reconnect and fail/recovery behavior on real Windows before claiming anti-cheat enforcement.

## Verification

```sh
dotnet test native-client/src/SafeExam.Tests/SafeExam.Tests.csproj -c Release
```

[Audit fixes and limits](AUDIT_FIXES.md).
