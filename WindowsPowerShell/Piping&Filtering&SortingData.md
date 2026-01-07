PowerShell uses piping (|) to send the output of one cmdlet as input to another. 

Where-Object filters the files by their Extension property, ensuring that only files with extension equal (-eq) to .txt are listed.

Common Commands:

Sort-Object (sorts objects by property) – no direct CMD equivalent, similar to sort in Linux.

Where-Object (filter objects based on conditions) – similar to grep in Linux.

Select-Object (select properties from objects) – used for refining output.

Example:

Get-ChildItem | Where-Object -Property Length -gt 100: List files greater than 100 bytes in size.

------------------------------------------------------

How would you retrieve the items in the current directory with size greater than 100? [for the sake of this question, avoid the use of quotes (“ or ‘) in your answer]

Answer: Get-ChildItem | Where-Object -Property Length -gt 100


