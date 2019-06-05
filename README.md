# cryo

Tool to automatically dump and restore a macOS environment.

### $HOME/.cryo/

#### config.

#### sleep

This is triggered before going into cryo sleep.

#### wakeup

This is triggered after waking up from cryo sleep.

### API

```
$ cryo [api]
```

#### init

Initializes `$HOME/.cryo/` directory.

#### sleep [target]

Dump the environment to the `[target]` drive.

1) This triggers `$HOME/.cryo/sleep` if present.
2) This dumps the `$HOME/.cryo` directory.
3) This prompts you for a secret to encrypt the dump with.

#### wakeup [target]

Restore the environment from the target drive.

1) This prompts you to enter a secret if the dump is encrypted.
2) This restores the `$HOME/.cryo` directory.
3) This triggers `$HOME/.cryo/wakeup` if present.
