---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
online version: 
schema: 2.0.0
---

# New-AzureRmDataLakeAnalyticsAccount
## SYNOPSIS
Creates a new Data Lake Analytics account.

## SYNTAX

```
New-AzureRmDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-DefaultDataLakeStore] <String> [[-Tags] <Hashtable[]>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>]
```

## DESCRIPTION
The New-AzureRmDataLakeAnalyticsAccount cmdlet creates a new Azure Data Lake Analytics account.

## EXAMPLES

### --------------------------  Example 1: Create a Data Lake Analytics account  --------------------------
@{paragraph=PS C:\\\>}

```
PS C:\> New-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount" `
               -ResourceGroupName "ContosoOrg" `
               -Location "East US 2" `
               -DefaultDataLake ContosoAdlStore `
```

This command creates a Data Lake Analytics account named ContosoAdlAccount that uses the ContosoAdlStore Data Store, in the resource group named ContosoOrg.

## PARAMETERS

### -ResourceGroupName
Specifies the resource group name of the Data Lake Analytics account.
To create a resource group, use the New-AzureRmResourceGroup cmdlet.

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

### -Name
Specifies the Data Lake Analytics account name.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Location
Specifies the location at which to create the Data Lake Analytics account.
Only East US 2 is supported at this time.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
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

Required: True
Position: 3
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
Position: 4
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

[Set-AzureRmDataLakeAnalyticsAccount]()

[Test-AzureRmDataLakeAnalyticsAccount]()

