# iis-lister
IIS directory lister (alternative for h5ai on IIS by ASP not PHP) - clone of iis-edb [https://code.google.com/p/iis-edb/] by Dale C. Anderson licensed under GNU GPL v3 adapted for KSI UJ needs

## original description
The Enhanced Directory Browser is a drop-in replacement for IIS's built-in directory browsing function. The major enhancements over IIS's built-in directory index are:
  - Files and folders are differentiated from each other.
  - Files / Folders are Sortable by Name, Date, and File Size.
  - Directory byte sizes are shown
  - The look and feel is totally customizable (not through configuration, but because you can change the source code)
  - Allows specific files / folders to be hidden via script configuration

Security Notes
  - It is very important to realize that this script is not aware of the IIS "Directory Browsing" directive. This means that if you have any files / folders that you do NOT want browsed, you need to do one of the following:
   - make sure your NT permissions are set correctly. (no script can override NT permissions)
   - Specify folders to be "hidden" in the script configuration.
  - If you want the script to present the user with a logon prompt for certain directories, you need to deny IUSR_<machinename> read access for those directories, since it's the IIS process that is accessing that folder by default.
  - The EDB will not browse to a higher-level directory than the directory in which the script is placed, even if a malicious user tries to manipulate the URL passed to it.

Installation
  - To install, download and unrar the latest version from the download folder into any folder on your web server that you want to be able to browse. The directory browser is recursive. Drop the EDB into any folder on your website, and you will be able to browse all of that folder's files and subfolders PROVIDED that "default.asp" is in the server's list of default documents, and that ASP is enabled on the server.

Configuration
  - For most people, the default out-of-the-box configuration will be sufficient. There are a few configuration options near the top of the script that you may find useful. As with any ASP script, use your favorite source code viewer, and edit to your heart's content.

## changes and plans
  - translation to polish - DONE
  - styling - DONE but could be better
  - IP blocking roules - IN PROGRESS
  - better handling source code files in weird languages (like Scala) - TODO
