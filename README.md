### To reproduce

1. Use pyinstaller to build `simple.py` (`pyinstaller -F simple.py`)
1. Place binary in src-tauri/bin
1. Append target triple (I'm on ARM mac so left my binary in there)
1. Run `yarn tauri dev`, see that sidecar command is successful
1. Make any change to `simple.py` (change printed text or whatever)
1. Repeat steps 2-4
1. See that sidecar fails with signal 9

Note:

- The binary still works normally when called from the terminal
- The sidecar works in the prod build `yarn tauri build`
- The sidecar only fails in dev `yarn tauri dev`

If I reboot my computer the binary will work again without changing the binary at all. It makes me wonder if it's somehow related to signing the binary? Thanks for any help.
