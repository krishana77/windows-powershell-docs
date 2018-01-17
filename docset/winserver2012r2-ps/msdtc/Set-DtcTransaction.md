---
external help file: MSFT_DtcTransactionTask_v1.0.cdxml-help.xml
Module Name: MsDtc
online version: 
schema: 2.0.0
title: Set-DtcTransaction
description: 
keywords: powershell, cmdlet
author: brianlic
manager: alanth
ms.date: 2017-10-29
ms.topic: reference
ms.prod: powershell
ms.technology: powershell
ms.assetid: BA7E24DE-F643-43A0-8F61-60AA7ACF6A1E
---

# Set-DtcTransaction

## SYNOPSIS
Modifies the state of a transaction.

## SYNTAX

### TraceSet
```
Set-DtcTransaction [-DtcName <String>] -TransactionId <Guid> [-Trace] [-CimSession <CimSession[]>]
 [-ThrottleLimit <Int32>] [-AsJob] [<CommonParameters>]
```

### ForgetSet
```
Set-DtcTransaction [-DtcName <String>] -TransactionId <Guid> [-Forget] [-CimSession <CimSession[]>]
 [-ThrottleLimit <Int32>] [-AsJob] [<CommonParameters>]
```

### CommitSet
```
Set-DtcTransaction [-DtcName <String>] -TransactionId <Guid> [-Commit] [-CimSession <CimSession[]>]
 [-ThrottleLimit <Int32>] [-AsJob] [<CommonParameters>]
```

### AbortSet
```
Set-DtcTransaction [-DtcName <String>] -TransactionId <Guid> [-Abort] [-CimSession <CimSession[]>]
 [-ThrottleLimit <Int32>] [-AsJob] [<CommonParameters>]
```

## DESCRIPTION
The **Set-DtcTransaction** cmdlet modifies the state of a transaction in the Distributed Transaction Coordinator (DTC) host-level properties stored in the registry.

## EXAMPLES

### Example 1: Set a trace for a transaction
```
PS C:\> Set-DtcTransaction -DtcName "Local" -Trace -TransactionId 2E6E62E0-044B-4DFE-9A8B-B69CFF5C9E26
```

This command sets a trace for the specified transaction.

## PARAMETERS

### -Abort
Indicates to abort the specified transaction.

```yaml
Type: SwitchParameter
Parameter Sets: AbortSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AsJob
{{Fill AsJob Description}}

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CimSession
Runs the cmdlet in a remote session or on a remote computer.
Enter a computer name or a session object, such as the output of a New-CimSessionhttp://go.microsoft.com/fwlink/p/?LinkId=227967 or Get-CimSessionhttp://go.microsoft.com/fwlink/p/?LinkId=227966 cmdlet.
The default is the current session on the local computer.

```yaml
Type: CimSession[]
Parameter Sets: (All)
Aliases: Session

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Commit
Specifies to commit the specified transaction.

```yaml
Type: SwitchParameter
Parameter Sets: CommitSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DtcName
Specifies a DTC instance.
The cmdlet modifies the state of a transaction in the DTC host-level properties for this instance.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Forget
Indicates to forget the specified transaction.

```yaml
Type: SwitchParameter
Parameter Sets: ForgetSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ThrottleLimit
Specifies the maximum number of concurrent operations that can be established to run the cmdlet.
If this parameter is omitted or a value of `0` is entered, then Windows PowerShell® calculates an optimum throttle limit for the cmdlet based on the number of CIM cmdlets that are running on the computer.
The throttle limit applies only to the current cmdlet, not to the session or to the computer.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Trace
Specifies to trace the transaction.

```yaml
Type: SwitchParameter
Parameter Sets: TraceSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TransactionId
Specifies the TransactionId of the transaction to modify.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-DtcTransaction](./Get-DtcTransaction.md)
