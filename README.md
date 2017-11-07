# TFS 2017 Theme Color Updater
Powershell script to change the theme color of TFS 2017 (useful and recommended only for test servers!)

# General Description
The repository contain two scripts: 
- Tfs2017ThemeColorUpdater.ps1 - Update the current TFS theme colors
- Tfs2017ThemeColorRestore.ps1 - Restore the TFS theme colors

# Tfs2017ThemeColorUpdater.ps1
This script perform the following steps: 
1.	Create a backup for the current theme (run only once - to backup the default theme)
2.	Update the ccs files (replace the current colors with the specified colors in all the css files)
3.	Restart the TFS server in order to apply the changes
Note: If you delete the backup folder, you will not be able to restore the default values

# Tfs2017ThemeColorRestore.ps1
This script perform the following steps: 
1.	Restore the current theme with the backup created by the another script
2.	Restart the TFS server in order to apply the changes

# Using
- Both scripts must be executed directly in the application server with administrator privileges  
- All the parameters are optional and receive default values

### Tfs2017ThemeColorUpdater.ps1

Parameters

- CurrentWelcomeColor: Current color of the welcome page (default: #106ebe)
- CurrentPrimaryColor: Current color of the header primary color (default: #0078d7)
- CurrentSecondaryColor: Current color of the header secondary color (default: #005a9e)
- NewWelcomeColor: New color for the welcome page (default: #D7000C)
- NewPrimaryColor: New color for the header primary color (default: #D7000C)
- NewSecondaryColor: New color for the header secondary color (default: #AC000A)
- TfsPath: Team Foundation Server path (default: "C:\Program Files\Microsoft Team Foundation Server 15.0")
- AppThemesPath: Path of the App_Themes folder (default: "C:\Program Files\Microsoft Team Foundation Server 15.0\Application Tier\Web Services\_static\tfs\Dev15.M125.1\App_Themes")

### Tfs2017ThemeColorRestore.ps1

Parameters

- TfsPath: Team Foundation Server path (default: "C:\Program Files\Microsoft Team Foundation Server 15.0")
- AppThemesPath: Path of the App_Themes folder (default: "C:\Program Files\Microsoft Team Foundation Server 15.0\Application Tier\Web Services\_static\tfs\Dev15.M125.1\App_Themes")
