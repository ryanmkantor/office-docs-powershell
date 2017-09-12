---
external help file: sharepoint.xml
online version: http://technet.microsoft.com/EN-US/library/55060c1d-4024-438e-b31d-6854df8b00d5(Office.15).aspx
schema: 2.0.0
---

# Start-SPTimerJob

## SYNOPSIS
Below Content Applies To: SharePoint Server 2013

## SYNTAX

```
Start-SPTimerJob [-Identity] <SPTimerJobPipeBind> [-AssignmentCollection <SPAssignmentCollection>] [-Confirm]
 [-WhatIf]
```

## DESCRIPTION
The Start-SPTimerJob cmdlet runs a timer job once on each front-end Web server where the parent service is provisioned.

For permissions and the most current information about Windows PowerShell for SharePoint Products, see the online documentation at http://go.microsoft.com/fwlink/p/?LinkId=251831 (http://go.microsoft.com/fwlink/p/?LinkId=251831).

## EXAMPLES

### -----------------EXAMPLE---------------- (SharePoint Server 2013)
```
C:\PS>Get-SPTimerJob job-recycle-bin-cleanup | Start-SPTimerJob
```

This example starts the timer job named, job-recycle-bin-cleanup.

### -----------------EXAMPLE---------------- (SharePoint Server 2016)
```
C:\PS>Get-SPTimerJob job-recycle-bin-cleanup | Start-SPTimerJob
```

This example starts the timer job named, job-recycle-bin-cleanup.

## PARAMETERS

### -Identity
Specifies the timer job to run.

The type must be a valid GUID, in the form 12345678-90ab-cdef-1234-567890bcdefgh; a valid name of a timer job (for example, TimerJob1); or an instance of a valid SPTimerJob object.

```yaml
Type: SPTimerJobPipeBind
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -AssignmentCollection
Manages objects for the purpose of proper disposal.
Use of objects, such as SPWeb or SPSite, can use large amounts of memory and use of these objects in Windows PowerShell scripts requires proper memory management.
Using the SPAssignment object, you can assign objects to a variable and dispose of the objects after they are needed to free up memory.
When SPWeb, SPSite, or SPSiteAdministration objects are used, the objects are automatically disposed of if an assignment collection or the Global parameter is not used.

When the Global parameter is used, all objects are contained in the global store.
If objects are not immediately used, or disposed of by using the Stop-SPAssignment command, an out-of-memory scenario can occur.

```yaml
Type: SPAssignmentCollection
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Confirm
Prompts you for confirmation before executing the command.
For more information, type the following command: get-help about_commonparameters

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Displays a message that describes the effect of the command instead of executing the command.
For more information, type the following command: get-help about_commonparameters

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS
