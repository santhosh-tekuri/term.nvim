## Plugin ID

manage terminal easily. each terminal buffer is given custom name by user

```text
santhosh-tekuri/term.nvim
https://github.com/santhosh-tekuri/term.nvim
```

## Commands

`ToogleTerm`: suggested keymap `ctrl+/`  
`PickTerm`: opens terminal picker. suggested keymap `ctrl+shift+/`  
`SafeQuit`: quit only if no terminal is open. if nvim is remoteUI, it detaches instead of quit, suggested keymap `<leader>q`  
`RunCmd`: open fullscreen terminal buffer with given command. add bang to omit `[Process Exited]`  

## in terminal window:
`ctrl+]` switch to normal mode  
`ctrl+n` new terminal  
`ctrl+,` prev terminal  
`ctrl+.` next terminal  

## Sample Configuration

there is no `setup` function

```lua
vim.keymap.set({ "n", "t" }, "<c-/>", "<CMD>ToggleTerm<cr>")
vim.keymap.set({ "n", "t" }, "<c-s-/>", "<CMD>PickTerm<cr>")
vim.keymap.set("n", "<leader>q", "<CMD>SafeQuit<cr>")
vim.keymap.set('n', '<leader>G', "<cmd>RunCmd! lazygit<cr>", { desc = "launch lazygit" })
```
