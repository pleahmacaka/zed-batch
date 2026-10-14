## Zed Windows Batch Extension

[![Zed download chart](https://zedbadge.dev/chart/windows-batch.svg)](https://zedbadge.dev/)  
*Made with 💙 [ZedBadge.dev](https://zedbadge.dev/) 💙*


## Running

Click the play button on the first line, or pick a task from `task: spawn`.

`Run <file> as Administrator` opens a separate elevated window by default. 
To keep it in Zed's terminal, set 
[sudo for Windows](https://learn.microsoft.com/en-us/windows/advanced-settings/sudo) 
to Inline (Windows 11 24H2+). Run this once in an elevated terminal:

```
sudo config --enable normal
```

To run with F7 and as Administrator with Ctrl+F7 in batch files, add this to `keymap.json`.
Keep `$ZED_FILENAME` as written:

```json
{
  "context": "Editor && (extension == bat || extension == cmd)",
  "bindings": {
    "f7": "editor::SpawnNearestTask",
    "ctrl-f7": ["task::Spawn", { "task_name": "Run $ZED_FILENAME as Administrator" }]
  }
}
```

Any other key works too, such as F5. Pick one that isn't already bound,
since this binding overrides it in batch files. F5, for example, is Zed's debugger key.

## Author
[![Zed author badge](https://zedbadge.dev/author/pleahmacaka.svg)](https://zedbadge.dev/)  

## License

[MIT](./LICENSE)
