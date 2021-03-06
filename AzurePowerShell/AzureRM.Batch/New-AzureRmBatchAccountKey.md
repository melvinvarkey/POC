---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
online version: 
schema: 2.0.0
---

# New-AzureRmBatchAccountKey
## SYNOPSIS
Regenerates a key of a Batch account.

## SYNTAX

```
New-AzureRmBatchAccountKey [-AccountName] <String> [-ResourceGroupName <String>] -KeyType <String>
```

## DESCRIPTION
The New-AzureRmBatchAccountKey cmdlet regenerates the primary or secondary key of an Azure Batch account.
The cmdlet returns a BatchAccountContext object that has its current PrimaryAccountKey and SecondaryAccountKey properties.

## EXAMPLES

### --------------------------  Example 1: Regenerate the primary account key on a Batch account  --------------------------
@{paragraph=PS C:\\\>}

```
PS C:\>New-AzureRmBatchAccountKey -AccountName "pfuller" -KeyType "Primary"
          AccountName                  : pfuller

          Location                     : westus

          ResourceGroupName            : CmdletExampleRG

          CoreQuota                    : 20

          PoolQuota                    : 20

          ActiveJobAndJobScheduleQuota : 20

          Tags                         :
          TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

This command regenerates the primary account key on the Batch account named pfuller.

## PARAMETERS

### -AccountName
Specifies the name of the Batch account for which this cmdlet regenerates a key.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -KeyType
Specifies the type of key that this cmdlet regenerates.
Valid values are:

-- Primary
            -- Secondary

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Specifies the resource group of the account for which this cmdlet regenerates a key.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## INPUTS

## OUTPUTS

### BatchAccountContext

## NOTES

## RELATED LINKS

[Get-AzureRmBatchAccountKeys]()

[Azure Batch Cmdlets]()

