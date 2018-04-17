---
external help file: Microsoft.PowerBI.Commands.Workspaces.dll-Help.xml
Module Name: MicrosoftPowerBIMgmt.Workspaces
online version:
schema: 2.0.0
---

# Get-PowerBIWorkspace

## SYNOPSIS
Returns a list of Power BI workspaces.

## SYNTAX

### List (Default)
```
Get-PowerBIWorkspace [-Scope <PowerBIUserScope>] [-Filter <String>] [-User <String>] [-Deleted] [-Orphaned]
 [-First <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

### Id
```
Get-PowerBIWorkspace -Id <Guid> [-Scope <PowerBIUserScope>] [<CommonParameters>]
```

### Name
```
Get-PowerBIWorkspace -Name <String> [-Scope <PowerBIUserScope>] [<CommonParameters>]
```

## DESCRIPTION
Retrieves a list of Power BI workspaces with the provided search criteria and scope specified.
You must have logged in previously before using, Login-PowerBIServiceAccount.

## EXAMPLES

### Example 1
```powershell
PS C:\> Get-PowerBIWorkspace
```

Returns all Power BI workspaces the calling user is assigned to (-Scope Individual).

### Example 2
```powershell
PS C:\> Get-PowerBIWorkspace -Scope Organization -Filter "tolower(name) eq 'contoso sales'"
```

Returns a workspace named 'Contoso Sales' (case insensitive with tolower) within the user's organization.

## PARAMETERS

### -Deleted
Indicates to show only deleted workspaces. Only supported when -Scope Organization is specified.

```yaml
Type: SwitchParameter
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Filter
OData filter, case-sensitive (element names start lowercase). Only supported when -Scope Organization is specified.

```yaml
Type: String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -First
First (top) list of results.

```yaml
Type: Int32
Parameter Sets: List
Aliases: Top

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Id
Id of the workspace to return.

```yaml
Type: Guid
Parameter Sets: Id
Aliases: GroupId, WorkspaceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Name of the workspace to return if one exists with that name. Case insensitive search.

```yaml
Type: String
Parameter Sets: Name
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Orphaned
Indicates to show only orphaned workspaces. Only supported when -Scope Organization is specified.

```yaml
Type: SwitchParameter
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Scope
Indicates scope of the call. Individual returns only workspaces assigned to them; Organization returns all workspaces within a tenant (must be an administrator to initiate). Individual is the default.

```yaml
Type: PowerBIUserScope
Parameter Sets: (All)
Aliases:
Accepted values: Individual, Organization

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Skip
Skips the first set of results.

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -User
Filter groups to show ones with the user is contained within. Only available when -Scope is Organization.

```yaml
Type: String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS

### System.Collections.Generic.IEnumerable`1[[Microsoft.PowerBI.Api.V2.Models.Group, Microsoft.PowerBI.Api, Version=2.0.10.18022, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]

## NOTES

## RELATED LINKS