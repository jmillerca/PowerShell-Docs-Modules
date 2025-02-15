﻿---
external help file: Microsoft.PowerShell.PlatyPS.dll-Help.xml
online version: https://learn.microsoft.com/powershell/module/microsoft.powershell.platyps/compare-commandhelp?view=ps-modules&WT.mc_id=ps-gethelp
Locale: en-US
Module Name: Microsoft.PowerShell.PlatyPS
ms.custom: preview1
ms.date: 10/25/2024
schema: 2.0.0
title: Compare-CommandHelp
---

# Compare-CommandHelp

## SYNOPSIS

Compares two **CommandHelp** objects and produces a detailed report showing the differences.

## SYNTAX

### __AllParameterSets

```
Compare-CommandHelp [-ReferenceCommandHelp] <CommandHelp> [-DifferenceCommandHelp] <CommandHelp>
 [-PropertyNamesToExclude <string[]>] [<CommonParameters>]
```

## DESCRIPTION

`Compare-CommandHelp` is a troubleshooting tool that compares two CommandHelp objects and produces a
detailed report showing the differences. For example, you can use this to compare objects imported
from different sources, such as two different versions of Markdown files.

## EXAMPLES

### Example 1

```powershell
$refcmd = Import-MarkdownCommandHelp -Path .\v1\Microsoft.PowerShell.PlatyPS\Compare-CommandHelp.md
$diffcmd = Import-MarkdownCommandHelp -Path .\v2\Microsoft.PowerShell.PlatyPS\Compare-CommandHelp.md
Compare-CommandHelp -ReferenceCommandHelp $refcmd -DifferenceCommandHelp $diffcmd > .\diff.log
```

## PARAMETERS

### -DifferenceCommandHelp

The CommandHelp object to compare against the reference object.

```yaml
Type: Microsoft.PowerShell.PlatyPS.Model.CommandHelp
Parameter Sets: (All)
Aliases:
Accepted values:
Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PropertyNamesToExclude

A list of one or more property names to exclude from the comparison.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values:
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReferenceCommandHelp

The base CommandHelp object to be compared to the difference object.

```yaml
Type: Microsoft.PowerShell.PlatyPS.Model.CommandHelp
Parameter Sets: (All)
Aliases:
Accepted values:
Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters

This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable,
-InformationAction, -InformationVariable, -OutBuffer, -OutVariable, -PipelineVariable,
-ProgressAction, -Verbose, -WarningAction, and -WarningVariable. For more information, see
[about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### Microsoft.PowerShell.PlatyPS.Model.CommandHelp

## OUTPUTS

### System.String

## NOTES

## RELATED LINKS

- [Import-MarkdownCommandHelp](Import-MarkdownCommandHelp.md)
- [Import-YamlCommandHelp](Import-YamlCommandHelp.md)
