<span id="_Toc498953343" class="anchor"></span>

# Logging

The logging capability provided by the Microsoft Dynamics GP web client installation can help you troubleshoot issues that users may experience with the Microsoft Dynamics GP web client. Information about logging is divided into the following topics:

-   [Logging overview](#logging-overview)  

-   [Enabling logging for a tenant](#enabling-logging-for-a-tenant)  

-   [Enabling logging for a session](#enabling-logging-for-a-session)  

## Logging overview

To effectively use logging, a basic understanding of the logging features is helpful.

### Levels of logging

Logging can be configured at multiple levels for a web client installation:

-   At the top level, you can enable logging for all of the users of a specific tenant.

-   If you are using multitenant environment, you can enable logging for specific users of a tenant.

-   At the lowest level, you can enable logging for a specific web client session.

### Types of logs

The following types of logs are available:

**Runtime Log**   Provides details about the actions performed by the web client runtime process.

**Script Log**   Contains a record of all of the sanScript scripts that are run by the Microsoft Dynamics GP web client runtime process.

**Timing Log**   Contains timing details for web client operations. Microsoft can analyze this information to isolate issues with web client performance.

**SQL Log**   Contains a record of all of the SQL statements there were issues by the Microsoft Dynamics GP web client runtime process.

### Log location

The logs are generated on the session host machine where the web client session is being run. The default location for the log files is:

C:\\ProgramData\\Microsoft Dynamics\\GPSessions\\Logs

To view the ProgramData folder, you will need to show the hidden files and folders on the session host machine.

## Enabling logging for a tenant

The tenant configuration you are using determines how you enable logging for the tenant.

### Single tenant

If you are using the Microsoft Dynamics GP web client in a single tenant configuration (not using the Tenant Service), you can enable logging for all users of the installation. Settings in the TenantConfiguration.xml file of the web client installation control the logging. This file is typically found in this location on the machine that is hosting the the web site for the web client installation:

C:\\Program Files\\Microsoft Dynamics\\GP Web Client\\GPweb\\

The &lt;RuntimeLogEnabled&gt; element in the TenantConfiguration.xml file controls logging for all users of the web client installation. When it has the value true, the runtime log is generated for every web client user.

The &lt;CustomRuntimeSettings&gt; element controls whether the other log types are generated. If the setting for the specific log type is set to true, that log will be generated.

If logging for a tenant is enabled for an extended time, the quantity and size of the log files generated can become very large. Be sure to disable logging after it is no longer needed.

The following example shows the settings in the TenantConfiguration.xml file that cause all of the logs to be generated.

&lt;RuntimeLogEnabled&gt;true&lt;/RuntimeLogEnabled&gt;

&lt;CustomRuntimeSettings&gt;ScriptLogEnabled=true|TimingLogEnabled=true| SqlLogEnabled=true&lt;/CustomRuntimeSettings&gt;

### Multiple tenants

If you are using the Microsoft Dynamic GP web client in a multitenant configuration, you can enable logging for a specific tenant or for specific users of the tenant. You will do this using the Tenant Management snap-in for the Web Management Console. Refer to the Tenant Services Installation and Administration Guide or the Tenant Management snap-in help for information about how to configure logging in a multitenant configuration.

## Enabling logging for a session

The Session Management snap-in of the Web Management Console is used to enable logging for a specific web client session. To enable logging for a session, complete the following procedure:

1. Select the session that you want to enable logging for.

2. In the ribbon, click Logging.

3. In the Logging Settings window, select the log types that you want to create.

4. Click OK. The logging for the session will begin.

![displays a lightbulb to indication tips and tricks.](media/lightbulb.png "Lightbulb symbol")Be sure that you disable logging when you have finished creating the logs.  
