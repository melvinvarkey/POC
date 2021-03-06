---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
online version: 
schema: 2.0.0
---

# Set-AzureRmDataLakeAnalyticsAccount
## SYNOPSIS
Modifies a Data Lake Analytics account.

## SYNTAX

```
Set-AzureRmDataLakeAnalyticsAccount [-Name] <String> [[-DefaultDataLakeStore] <String>] [[-Tags] <Hashtable[]>]
 [[-ResourceGroupName] <String>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
```

## DESCRIPTION
The Set-AzureRmDataLakeAnalyticsAccount cmdlet modifies an Azure Data Lake Analytics account.

## EXAMPLES

### --------------------------  Example 1: Modify the data source of an account  --------------------------
@{paragraph=PS C:\\\>}

```
PS C:\> Set-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAcct" `
                    -DefaultDataLake "ContosoAdlStore01" `
                    -Tags @{"stage"="production"}
```

This command changes the default data source and the Tags property of the account.

## PARAMETERS

### -Name
Specifies the Data Lake Analytics account name.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultDataLakeStore
Specifies the name of the Data Lake Store account to set as the default data source.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: 
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tags
Specifies key-value pairs that can be used to identify the Data Lake Analytics account among other Azure resources.

```yaml
Type: Hashtable[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Specifies the resource group name of the Data Lake Analytics account.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InformationAction
@{Text=}

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: 
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
@{Text=}

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: 
Accept pipeline input: False
Accept wildcard characters: False
```

## INPUTS

## OUTPUTS

## NOTES

## RELATED LINKS

[Get-AzureRmDataLakeAnalyticsAccount]()

[New-AzureRmDataLakeAnalyticsAccount]()

[Remove-AzureRmDataLakeAnalyticsAccount]()

[Test-AzureRmDataLakeAnalyticsAccount]()

