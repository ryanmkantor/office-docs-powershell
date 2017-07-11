---
applicable: Lync Server 2013, Skype for Business Server 2015
schema: 2.0.0
---

# Search-CsClsLogging

## SYNOPSIS
Below Content Applies To: Lync Server 2013

Provides a command-line option for searching the centralized logging service log files.
This cmdlet was introduced in Lync Server 2013 Preview.

Below Content Applies To: Skype for Business Server 2015

Provides a command-line option for searching the centralized logging service log files.
This cmdlet was introduced in Lync Server 2013.



## SYNTAX

```
Search-CsClsLogging [-AsXml] [-CallId <String>] [-Components <String[]>] [-Computers <String[]>]
 [-ConferenceId <String>] [-CorrelationIds <String[]>] [-EndTime <DateTime>] [-IP <IPAddress>]
 [-LogLevel <String>] [-MatchAll] [-MatchAny] [-OutputFilePath <String>] [-Phone <String>] [-Pools <String[]>]
 [-SipContents <String>] [-SkipNetworkLogs] [-StartTime <DateTime>] [-Uri <String>] [<CommonParameters>]
```

## DESCRIPTION
Below Content Applies To: Lync Server 2013

The centralized logging service (which replaces the OCSLogger and OCSTracer tools used in Microsoft Lync Server 2010) provides a way for administrators to manage logging and tracing for all computers and pools running Microsoft Lync Server 2013 Preview.
Centralized logging enables administrators to stop, start, and configure logging for one or more pools and computers by using a single command; for example, you can use one command to enable Address Book service logging on all your Address Book servers.
This differs from the OCSLogger and OCSTracer tools, which had to be individually managed (including individually stopped and started) on each server.
In addition, the centralized logging service also provides a way for administrators to search trace logs from the command, using Windows PowerShell and the Search-CsClsLogging cmdlet.

Centralized logging is built around a series of predefined scenarios that offer a more finely-targeted approach to logging than offered in previous versions of Lync Server.
These scenarios predetermine the server components and logging for you; as a result, an administrator enabling the RGS scenario can be confident that he or she will only log information relevant to the Response Group service and not to, say, the audio conferencing provider service.

The Search-CsClsLogging cmdlet provides a command line option for searching the log files generated by the centralized logging service.

To return a list of all the role-based access control (RBAC) roles this cmdlet has been assigned to (including any custom RBAC roles you have created yourself), run the following command from the Windows PowerShell prompt:

Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Search-CsClsLogging"}

Lync Server Control Panel: The functions carried out by the Search-CsClsLogging cmdlet are not available in the Lync Server Control Panel.

Below Content Applies To: Skype for Business Server 2015

The centralized logging service (which replaces the OCSLogger and OCSTracer tools used in Microsoft Lync Server 2010) provides a way for administrators to manage logging and tracing for all computers and pools running Skype for Business Server 2015.
Centralized logging enables administrators to stop, start, and configure logging for one or more pools and computers by using a single command; for example, you can use one command to enable Address Book service logging on all your Address Book servers.
This differs from the OCSLogger and OCSTracer tools, which had to be individually managed (including individually stopped and started) on each server.
In addition, the centralized logging service also provides a way for administrators to search trace logs from the command, using the Windows PowerShell command-line interface and the Search-CsClsLogging cmdlet.

Centralized logging is built around a series of predefined scenarios that offer a more finely-targeted approach to logging than offered in previous versions of Skype for Business Server 2015.
These scenarios predetermine the server components and logging for you; as a result, an administrator enabling the RGS scenario can be confident that he or she will only log information relevant to the Response Group service and not to, say, the audio conferencing provider service.

The Search-CsClsLogging cmdlet provides a command line option for searching the log files generated by the centralized logging service.

Skype for Business Server Control Panel: The functions carried out by the Search-CsClsLogging cmdlet are not available in the Skype for Business Server Control Panel.



## EXAMPLES

### -------------------------- Example 1 -------------------------- (Lync Server 2013)
```

```

The command shown in Example 1 searches for the IP address 192.168.0.242 in the log files found on the computer atl-cs-001.litwareinc.com.

Search-CsClsLogging -Computers "atl-cs-001.litwareinc.com" -IP "192.168.0.242"

### -------------------------- Example 1 -------------------------- (Skype for Business Server 2015)
```

```

The command shown in Example 1 searches for the IP address 192.168.0.242 in the log files found on the computer atl-cs-001.litwareinc.com.

Search-CsClsLogging -Computers "atl-cs-001.litwareinc.com" -IP "192.168.0.242"

### -------------------------- Example 2 -------------------------- (Lync Server 2013)
```

```

In Example 2, a search is made for entries that match both the IP address 192.168.0.242 and the Uri sip:kenmyer@litwareinc.com.
The MatchAll parameter specifies that all the criteria must be met for an entry to be recorded as a match.

Search-CsClsLogging -Computers "atl-cs-001.litwareinc.com" -IP "192.168.0.242" -Uri "sip:kenmyer@litwareinc.com" -MatchAll

### -------------------------- Example 2 -------------------------- (Skype for Business Server 2015)
```

```

In Example 2, a search is made for entries that match both the IP address 192.168.0.242 and the Uri sip:kenmyer@litwareinc.com.
The MatchAll parameter specifies that all the criteria must be met for an entry to be recorded as a match.

Search-CsClsLogging -Computers "atl-cs-001.litwareinc.com" -IP "192.168.0.242" -Uri "sip:kenmyer@litwareinc.com" -MatchAll

### -------------------------- Example 3 -------------------------- (Lync Server 2013)
```

```

The command shown in Example 3 searches for entries that match either the IP address 192.168.0.242 or the Uri sip:kenmyer@litwareinc.com.
The MatchAny parameter specifies that just one of the criteria must be met for an entry to be recorded as a match.

Search-CsClsLogging -Computers "atl-cs-001.litwareinc.com" -IP "192.168.0.242" -Uri "sip:kenmyer@litwareinc.com" -MatchAny

### -------------------------- Example 3 -------------------------- (Skype for Business Server 2015)
```

```

The command shown in Example 3 searches for entries that match either the IP address 192.168.0.242 or the Uri sip:kenmyer@litwareinc.com.
The MatchAny parameter specifies that just one of the criteria must be met for an entry to be recorded as a match.

Search-CsClsLogging -Computers "atl-cs-001.litwareinc.com" -IP "192.168.0.242" -Uri "sip:kenmyer@litwareinc.com" -MatchAny

## PARAMETERS

### -AsXml
When specified, return code information from each computer searched is returned in XML format instead of as a string value.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 
Applicable: Lync Server 2013, Skype for Business Server 2015

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CallId
Call identifier to be searched for.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Applicable: Lync Server 2013, Skype for Business Server 2015

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Components
Comma-separated list of components to be searched.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 
Applicable: Lync Server 2013, Skype for Business Server 2015

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Computers
Comma-separated list of the computers to be searched.
For example:

-Computers "server-cs-001.litwareinc.com", "server-cs-002.litwareinc.com"

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 
Applicable: Lync Server 2013, Skype for Business Server 2015

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConferenceId
Conference ID to be searched for.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Applicable: Lync Server 2013, Skype for Business Server 2015

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CorrelationIds
Comma-separated list of correlation IDs to search for.
A correlation is a 32 bit integer associated with each request.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 
Applicable: Lync Server 2013, Skype for Business Server 2015

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndTime
Below Content Applies To: Lync Server 2013

Ending date and time for the log entries to be searched.
Specified in local time zone.
Defaults to 5 minutes after current time if no StartTime specified, otherwise defaults to 30 minutes after StartTime.
For example, on computer running the US English version of Lync Server 2013 Preview, this syntax limits the search to entries recorded prior to 8:00 AM on August 31, 2012:

-StartTime "8/31/2012 8:00AM"



Below Content Applies To: Skype for Business Server 2015

Ending date and time for the log entries to be searched.
Specified in local time zone.
Defaults to 5 minutes after current time if no StartTime specified, otherwise defaults to 30 minutes after StartTime.
For example, on computer running the US English version of Skype for Business Server 2015, this syntax limits the search to entries recorded prior to 8:00 AM on August 31, 2012:

-StartTime "8/31/2012 8:00AM"



```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 
Applicable: Lync Server 2013, Skype for Business Server 2015

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IP
IP address being searched for.
This must be an actual IP address; you cannot use wildcards when specifying the address.

```yaml
Type: IPAddress
Parameter Sets: (All)
Aliases: 
Applicable: Lync Server 2013, Skype for Business Server 2015

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LogLevel
Below Content Applies To: Lync Server 2013

Specifies the minimum type of log entry to be returned.
Allowed values are:

* Fatal
* Error
* Warning
* Info
* Verbose
* Debug
* All

"Minimum type of entry to be returned" means that Search-CsClsLogging will return all log entries at that level of severity plus all log entries with a higher level of severity.
For example, if you set the LogLevel to Warning then the cmdlet will return entries marked as Fatal and Error as well as entries marked as Warning.



Below Content Applies To: Skype for Business Server 2015

Specifies the minimum type of log entry to be returned.
Allowed values are:

Fatal

Error

Warning

Info

Verbose

Debug

All

"Minimum type of entry to be returned" means that the Search-CsClsLogging cmdlet will return all log entries at that level of severity plus all log entries with a higher level of severity.
For example, if you set the LogLevel to Warning then the cmdlet will return entries marked as Fatal and Error as well as entries marked as Warning.



```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Applicable: Lync Server 2013, Skype for Business Server 2015

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MatchAll
When present, all the included criteria must be matched.
This is similar to an AND query in SQL Server.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 
Applicable: Lync Server 2013, Skype for Business Server 2015

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MatchAny
When present, only one of the included criteria must be matched.
This is similar to an OR query in SQL Server.
This is the default.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 
Applicable: Lync Server 2013, Skype for Business Server 2015

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OutputFilePath
When present, specifies the full path of where to write a text file containing the search results.
Otherwise they are written to the console.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Applicable: Lync Server 2013, Skype for Business Server 2015

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Phone
Phone number to be searched for.
This number should be entered using the E.164 format and should not include wildcard characters.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Applicable: Lync Server 2013, Skype for Business Server 2015

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Pools
Comma-separated list of the pools to be searched.
For example:

-Pools "atl-cs-001.litwareinc.com", "red-cs-001.litwareinc.com"

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 
Applicable: Lync Server 2013, Skype for Business Server 2015

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SipContents
Arbitrary text to search for within the body of a SIP message.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Applicable: Lync Server 2013, Skype for Business Server 2015

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkipNetworkLogs
Below Content Applies To: Lync Server 2013

When present, instructs Search-CsClsLogging to avoid searching network logs.



Below Content Applies To: Skype for Business Server 2015

When present, instructs the Search-CsClsLogging cmdlet to avoid searching network logs.



```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 
Applicable: Lync Server 2013, Skype for Business Server 2015

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartTime
Below Content Applies To: Lync Server 2013

Beginning date and time for the log entries to be searched.
Specified in local time zone.
Defaults to 30 minutes before EndTime.
For example, on computer running the US English version of Lync Server 2013 Preview, this syntax limits the search to entries recorded at 8:00 AM on or after August 1, 2012:

-StartTime "8/1/2012 8:00AM"



Below Content Applies To: Skype for Business Server 2015

Beginning date and time for the log entries to be searched.
Specified in local time zone.
Defaults to 30 minutes before EndTime.
For example, on computer running the US English version of Skype for Business Server 2015, this syntax limits the search to entries recorded at 8:00 AM on or after August 1, 2012:

-StartTime "8/1/2012 8:00AM"



```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 
Applicable: Lync Server 2013, Skype for Business Server 2015

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Uri
Uri to be searched for.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Applicable: Lync Server 2013, Skype for Business Server 2015

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

###  
None.
Search-CsClsLogging does not accept pipelined input.

###  
None.
The Search-CsClsLogging cmdlet does not accept pipelined input.

## OUTPUTS

###  
String values or XML.

## NOTES

## RELATED LINKS

[Show-CsClsLogging]()

[Start-CsClsLogging]()

[Stop-CsClsLogging]()

[Sync-CsClsLogging]()

[Update-CsClsLogging]()

[Online Version](http://technet.microsoft.com/EN-US/library/a2eddada-a494-4bc6-b7d0-9b511dfc4ac1(OCS.15).aspx)

[Online Version](http://technet.microsoft.com/EN-US/library/a2eddada-a494-4bc6-b7d0-9b511dfc4ac1(OCS.16).aspx)
