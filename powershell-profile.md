# Powershell Profile File

## `<code/notepad/zed> $PROFILE`

```powershell
$env:PATH += "C:\Program Files\Go\bin"
$env:PATH += ";C:\Users\jfalava\AppData\Local\Programs\oh-my-posh\bin"
$env:PATH += ";D:\02.Projects\zed\target\release"
#
function gitname {
    git config user.name "Jorge Fernando Álava"
}
New-Alias git-name gitname
function gitemail {
    git config user.name "git@jfa.dev"
}
New-Alias git-email gitemail
function ezals {
    eza --color=always --long --git --no-filesize --icons=always
}
New-Alias l ezals
function whichwin {
    param (
        [string]$name
    )
    Get-Command $name | Select-Object -ExpandProperty Definition
}
Set-Alias which whichwin
#
Import-Module posh-git
oh-my-posh init pwsh --config 'https://raw.githubusercontent.com/JanDeDobbeleer/oh-my-posh/main/themes/wopian.omp.json' | Invoke-Expression
#f45873b3-b655-43a6-b217-97c00aa0db58 PowerToys CommandNotFound module

Import-Module -Name Microsoft.WinGet.CommandNotFound
#f45873b3-b655-43a6-b217-97c00aa0db58
Clear-Host
#
Invoke-Expression (& { (zoxide init powershell | Out-String) })

```
