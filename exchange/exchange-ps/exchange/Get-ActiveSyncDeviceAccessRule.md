---
applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online
schema: 2.0.0
---

# Get-ActiveSyncDeviceAccessRule

## SYNOPSIS
!!! Exchange Server 2010

Use the Get-ActiveSyncDeviceAccessRule cmdlet to retrieve an access group of Exchange mobile devices along with their access level.

!!! Exchange Server 2013, Exchange Server 2016, Exchange Online

This cmdlet is available in on-premises Exchange and in the cloud-based service. Some parameters and settings may be exclusive to one environment or the other.

Use the Get-ActiveSyncDeviceAccessRule cmdlet to retrieve an access group of Exchange mobile devices along with their access level.

For information about the parameter sets in the Syntax section below, see Exchange cmdlet syntax (https://technet.microsoft.com/library/bb123552.aspx).

## SYNTAX

```
Get-ActiveSyncDeviceAccessRule [[-Identity] <ActiveSyncDeviceAccessRuleIdParameter>] [-DomainController <Fqdn>]
 [-Organization <OrganizationIdParameter>] [<CommonParameters>]
```

## DESCRIPTION
!!! Exchange Server 2010

You can create multiple groups of devices: allowed devices, blocked devices, and quarantined devices with the New-ActiveSyncDeviceAccessRule cmdlet. The Get-ActiveSyncDeviceAccessRule cmdlet retrieves the settings for any existing group.

You need to be assigned permissions before you can run this cmdlet. Although all parameters for this cmdlet are listed in this topic, you may not have access to some parameters if they're not included in the permissions assigned to you. To see what permissions you need, see the "Exchange ActiveSync settings" entry in the Client Access Permissions topic.

!!! Exchange Server 2013

You can create multiple groups of devices: allowed devices, blocked devices, and quarantined devices with the New-ActiveSyncDeviceAccessRule cmdlet. The Get-ActiveSyncDeviceAccessRule cmdlet retrieves the settings for any existing group.

You need to be assigned permissions before you can run this cmdlet. Although all parameters for this cmdlet are listed in this topic, you may not have access to some parameters if they're not included in the permissions assigned to you. To see what permissions you need, see the "Exchange ActiveSync settings" entry in the Clients and mobile devices permissions topic.

!!! Exchange Server 2016, Exchange Online

You can create multiple groups of devices: allowed devices, blocked devices, and quarantined devices with the New-ActiveSyncDeviceAccessRule cmdlet. The Get-ActiveSyncDeviceAccessRule cmdlet retrieves the settings for any existing group.

You need to be assigned permissions before you can run this cmdlet. Although this topic lists all parameters for the cmdlet, you may not have access to some parameters if they're not included in the permissions assigned to you. To find the permissions required to run any cmdlet or parameter in your organization, see Find the permissions required to run any Exchange cmdlet (https://technet.microsoft.com/library/mt432940.aspx).

## EXAMPLES

### Example 1 -------------------------- (Exchange Server 2010)
```
Get-ActiveSyncDeviceAccessRule | where {$_.AccessLevel -eq 'Block'}
```

This example lists all the rules currently blocking mobile phones.

### Example 1 -------------------------- (Exchange Server 2013)
```
Get-ActiveSyncDeviceAccessRule | where {$_.AccessLevel -eq 'Block'}
```

This example lists all the rules currently blocking mobile phones.

### Example 1 -------------------------- (Exchange Server 2016)
```
Get-ActiveSyncDeviceAccessRule | where {$_.AccessLevel -eq 'Block'}
```

This example lists all the rules currently blocking mobile phones.

### Example 1 -------------------------- (Exchange Online)
```
Get-ActiveSyncDeviceAccessRule | where {$_.AccessLevel -eq 'Block'}
```

This example lists all the rules currently blocking mobile phones.

### Example 2 -------------------------- (Exchange Server 2010)
```
Get-ActiveSyncDeviceAccessRule | Format-List Characteristic, QueryString, AccessLevel
```

This example lists all device access rules set up on the server.

### Example 2 -------------------------- (Exchange Server 2013)
```
Get-ActiveSyncDeviceAccessRule | Format-List Characteristic, QueryString, AccessLevel
```

This example lists all device access rules set up on the server.

### Example 2 -------------------------- (Exchange Server 2016)
```
Get-ActiveSyncDeviceAccessRule | Format-List Characteristic, QueryString, AccessLevel
```

This example lists all device access rules set up on the server.

### Example 2 -------------------------- (Exchange Online)
```
Get-ActiveSyncDeviceAccessRule | Format-List Characteristic, QueryString, AccessLevel
```

This example lists all device access rules set up on the server.

## PARAMETERS

### -DomainController
!!! Exchange Server 2010

The DomainController parameter specifies the domain controller that's used by this cmdlet to read data from or write data to Active Directory. You identify the domain controller by its fully qualified domain name (FQDN). For example, dc01.contoso.com.



!!! Exchange Server 2013, Exchange Server 2016, Exchange Online

This parameter is available only in on-premises Exchange.

The DomainController parameter specifies the domain controller that's used by this cmdlet to read data from or write data to Active Directory. You identify the domain controller by its fully qualified domain name (FQDN). For example, dc01.contoso.com.



```yaml
Type: Fqdn
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Identity
The Identity parameter specifies the unique identifier for the device access rule.

```yaml
Type: ActiveSyncDeviceAccessRuleIdParameter
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010, Exchange Server 2013, Exchange Server 2016, Exchange Online

Required: False
Position: 1
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### -Organization
This parameter is available for multi-tenant deployments. It isn't available for on-premises deployments. For more information about multi-tenant deployments, see Multi-Tenant Support.

The Organization parameter specifies the organization in which you'll perform this action. This parameter doesn't accept wildcard characters, and you must use the exact name of the organization.

```yaml
Type: OrganizationIdParameter
Parameter Sets: (All)
Aliases:
Applicable: Exchange Server 2010

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/p/?LinkID=113216).

## INPUTS

###  
To see the input types that this cmdlet accepts, see Cmdlet Input and Output Types (https://go.microsoft.com/fwlink/p/?LinkId=616387). If the Input Type field for a cmdlet is blank, the cmdlet doesn't accept input data.

## OUTPUTS

###  
To see the return types, which are also known as output types, that this cmdlet accepts, see Cmdlet Input and Output Types (https://go.microsoft.com/fwlink/p/?LinkId=616387). If the Output Type field is blank, the cmdlet doesn't return data.

## NOTES

## RELATED LINKS

[Online Version](https://technet.microsoft.com/library/f9bcb8d8-1239-43b8-9885-b655cbe8b4bc.aspx)

