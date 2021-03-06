---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
online version: 
schema: 2.0.0
---

# Remove-AzureBatchNodeFile
## SYNOPSIS
Deletes a node file for a task or compute node.

## SYNTAX

### Task
```
Remove-AzureBatchNodeFile -JobId <String> -TaskId <String> -Name <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-WhatIf] [-Confirm]
```

### ComputeNode
```
Remove-AzureBatchNodeFile [-PoolId] <String> [-ComputeNodeId] <String> -Name <String> [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-WhatIf] [-Confirm]
```

### InputObject
```
Remove-AzureBatchNodeFile [[-InputObject] <PSNodeFile>] [-Force] [-Recursive]
 -BatchContext <BatchAccountContext> [-WhatIf] [-Confirm]
```

## DESCRIPTION
The Remove-AzureBatchNodeFile cmdlet deletes an Azure Batch node file for a task or compute node.

## EXAMPLES

### --------------------------  Example 1: Delete a file assocated with a task  --------------------------
@{paragraph=PS C:\\\>}

```
PS C:\>Remove-AzureBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Name "wd\testFile.txt" -BatchContext $Context
```

This command deletes the node file that is named wd\testFile.txt.
That file is associated with the task that has the ID Task26 under the job Job-000001.

### --------------------------  Example 2: Delete a file from a compute node  --------------------------
@{paragraph=PS C:\\\>}

```
PS C:\>Remove-AzureBatchNodeFile -PoolId "Pool07" -ComputeNodeId "tvm-2316545714_1-20150725t213220z" -Name "startup\testFile.txt" -BatchContext $Context
```

This command deletes the node file that is named startup\testFile.txt from the specified compute node in the pool that has the ID Pool07.

### --------------------------  Example 3: Remove a file by using the pipeline  --------------------------
@{paragraph=PS C:\\\>}

```
PS C:\>Get-AzureBatchNodeFile -JobId "Job-000001" -TaskId "Task26" -Name "wd\testFile2.txt" -BatchContext $Context | Remove-AzureBatchNodeFile -Force -BatchContext $Context
```

This command gets the node file by using Get-AzureBatchNodeFile.
That file is associated with the task that has the ID Task26 under the job Job-000001.
The command passes that file to the current cmdlet by using the pipeline.
The current cmdlet removes the node file.
The command specifies the Force parameter.
Therefore, the command does not prompt you for confirmation.

## PARAMETERS

### -BatchContext
Specifies the BatchAccountContext instance that this cmdlet uses to interact with the Batch service.
To obtain a BatchAccountContext object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ComputeNodeId
Specifies the ID of the compute node that contains the Batch node file that this cmdlet deletes.

```yaml
Type: String
Parameter Sets: ComputeNode
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
Forces the command to run without asking for user confirmation.

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

### -InputObject
Specifies PSNodeFile object that represent the node file tha this cmdlet deletes.
To obtain a PSNodeFile, use the Get-AzureBatchNodeFile cmdlet.

```yaml
Type: PSNodeFile
Parameter Sets: InputObject
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -JobId
Specifies the ID of the job that contains the task.

```yaml
Type: String
Parameter Sets: Task
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Specifies the name of the node file that this cmdlet deletes.

```yaml
Type: String
Parameter Sets: Task, ComputeNode
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PoolId
Specifies the ID of the pool that contains the compute nodes for which this cmdlet removes a file.

```yaml
Type: String
Parameter Sets: ComputeNode
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Recursive
If the file path is a directory, delete the directory and all of the files and subdirectories in it.

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

### -TaskId
Specifies the ID of the task.

```yaml
Type: String
Parameter Sets: Task
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
{{Fill Confirm Description}}

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: 
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
{{Fill WhatIf Description}}

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

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

[Get-AzureRmBatchAccountKeys]()

[Get-AzureBatchNodeFile]()

[Get-AzureBatchNodeFileContent]()

