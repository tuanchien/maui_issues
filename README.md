Demo code created with
```
dotnet new maui -f net8.0 -n demo
```

The demo.csproj was edited to remove some targets other than net8.0-maccatalyst

In `MainPage.xaml.cs`, `OnCounterClicked` is changed to
```
private async void OnCounterClicked(object sender, EventArgs e)
```

with
```
var file = await FilePicker.Default.PickAsync();
```
added to the end of that method.


# Environment #
1. MacOS 15 (Sequoia)
1. Xcode 16. Behaviour present with Xcode 15.4 manually installed.
1. Checked with project templates generated against Microsoft.NETCore.App 8.0.8 and 9.0.0-rc.1.24431.7

# Expected behaviour #
Dialog box shows up to select a file when button clicked.

# Actual behaviour #
Nothing shows up once button is clicked, and buttons lose responsiveness.
