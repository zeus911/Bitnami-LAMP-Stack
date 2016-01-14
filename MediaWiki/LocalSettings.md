# my new add
$wgShowExceptionDetails = true;
# Enabled Extensions. Most extensions are enabled by including the base extension file here
# but check specific extension documentation for more details
# The following extensions were automatically enabled:
wfLoadExtension( 'Cite' );
wfLoadExtension( 'CiteThisPage' );
require_once "$IP/extensions/ConfirmEdit/ConfirmEdit.php";
wfLoadExtension( 'Gadgets' );
wfLoadExtension( 'ImageMap' );
wfLoadExtension( 'InputBox' );
wfLoadExtension( 'Interwiki' );
// To grant sysops permissions to edit interwiki data
$wgGroupPermissions['sysop']['interwiki'] = true;
wfLoadExtension( 'LocalisationUpdate' );
wfLoadExtension( 'Nuke' );
wfLoadExtension( 'ParserFunctions' );
$wgPFEnableStringFunctions = true;
wfLoadExtension( 'PdfHandler' );
wfLoadExtension( 'Poem' );
wfLoadExtension( 'Renameuser' );
wfLoadExtension( 'SpamBlacklist' );
wfLoadExtension( 'SyntaxHighlight_GeSHi' );
wfLoadExtension( 'TitleBlacklist' );
wfLoadExtension( 'WikiEditor' );
# Enables use of WikiEditor by default but still allow users to disable it in preferences
$wgDefaultUserOptions['usebetatoolbar'] = 1;
$wgDefaultUserOptions['usebetatoolbar-cgd'] = 1;
$wgDefaultUserOptions['wikieditor-preview'] = 1;
$wgDefaultUserOptions['wikieditor-publish'] = 1;
# End of automatically generated settings.
# Add more configuration options below.

# my new add site config 


# my new add extension 
# CodeEditor
wfLoadExtension( 'CodeEditor' );
$wgScribuntoUseCodeEditor = true;

# Scribunto 
require_once "$IP/extensions/Scribunto/Scribunto.php";
$wgScribuntoDefaultEngine = 'luastandalone';
$wgScribuntoUseGeSHi = true;
$wgScribuntoUseCodeEditor = true;

# UniversalLanguageSelector
require_once "$IP/extensions/UniversalLanguageSelector/UniversalLanguageSelector.php";

# VisualEditor
require_once "$IP/extensions/VisualEditor/VisualEditor.php";
$wgDefaultUserOptions['visualeditor-enable'] = 1;  // Enable by default for everybody
$wgHiddenPrefs[] = 'visualeditor-enable';   // Don't allow users to disable it
$wgDefaultUserOptions['visualeditor-enable-experimental'] = 1;  // OPTIONAL: Enable VisualEditor's experimental code features
$wgVisualEditorParsoidForwardCookies=true;   // Forwarding Cookies to Parsoid
# Parsoid
$wgVisualEditorParsoidURL = 'http://localhost:8000';   // Parsoid Dev for Ubuntu 
 
# MultimediaViewer
require_once "$IP/extensions/MultimediaViewer/MultimediaViewer.php";
 
# Collection 
require_once "$IP/extensions/Collection/Collection.php";
$wgEnableApi = true;

# MultiBoilerplate
wfLoadExtension( 'MultiBoilerplate' );
$wgMultiBoilerplateDiplaySpecialPage=true;
$wgMultiBoilerplateOverwrite=true;
$wgMultiBoilerplateOptions[ "New page" ] = "Template:New page";
 
# CategoryTree 
require_once "$IP/extensions/CategoryTree/CategoryTree.php";
$wgUseAjax = true;
 
# CheckUser
wfLoadExtension( 'CheckUser' );
 
# Delete Batch
require_once "$IP/extensions/DeleteBatch/DeleteBatch.php";
$wgGroupPermissions['bureaucrat']['deletebatch'] = false;
$wgGroupPermissions['sysop']['deletebatch'] = true;
 
# Disambiguator
wfLoadExtension( 'Disambiguator' );
 
# MobileFrontend
require_once "$IP/extensions/MobileFrontend/MobileFrontend.php";
$wgMFAutodetectMobileView = true;

# MsUpload
require_once "$IP/extensions/MsUpload/MsUpload.php";

$wgMSU_showAutoCat = true; // If true, files uploaded while editing a category will be added to that category
$wgMSU_checkAutoCat = true; // Whether the checkbox for the above mentioned case is checked by default
$wgMSU_imgParams = '400px'; // The default parameters for inserted images
$wgMSU_useDragDrop = true; // Should the drag & drop area be shown?
$wgMSU_useMsLinks = false; // Should we allow to insert links in the style of the Extension:MsLinks?

$wgEnableWriteAPI = true; // Enable the API
$wgEnableUploads = true; // Enable uploads
$wgAllowJavaUploads = true; // Solves problem with Office 2007 and newer files (docx, xlsx, etc.)
$wgGroupPermissions['user']['upload'] = true; // Allow regular users to upload files
// Make sure that the file types you want to upload are allowed:
$wgFileExtensions = array( 'bmp', 'doc', 'docx', 'flac', 'gif', 'ico', 'jpeg', 'jpg', 'mp3', 'mpp', 'odg', 'odp', 'ods', 'odt', 'ogg', 'pdf', 'png', 'ppt', 'pptx', 'ps', 'rtf', 'svg', 'swf', 'tif', 'tiff', 'xls', 'xlsx', 'xml' );

# CharInsert
wfLoadExtension( 'CharInsert' );

# ParsoidBatchAPI
wfLoadExtension( 'ParsoidBatchAPI' );