PowerShell uses cmdlets (command-lets), which follow a consistent Verb-Noun naming convention, making commands easier to understand.

example: Get-Content, Get- Verb, Content - Noun

Common Commands:

Get-Content (read file content) – similar to type in CMD and cat in Linux.

Set-Location (change directory) – similar to cd in CMD/Linux.

Get-Command (list all commands) – helps discover available cmdlets.

Get-help [command] - display option of this command

------------------------------------------------
How would you retrieve a list of commands that start with the verb Remove? [for the sake of this question, avoid the use of quotes (" or ') in your answer]

Answer: Get-Command -Verb Remove

What cmdlet has its traditional counterpart echo as an alias?

Answer: Write-Output

Get-Alias -Name echo*

What is the command to retrieve some example usage for the cmdlet New-LocalUser?

Answer: Get-Help New-LocalUser -examples
