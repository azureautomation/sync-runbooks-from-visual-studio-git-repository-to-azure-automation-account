Sync runbooks from Visual Studio Git repository to Azure Automation Account
===========================================================================

            

**Description**


This runbook syncs all runbooks from a Visual Studio online (VSO) Git repository to an existing Azure Automation account starting with dependent (child) runbooks and followed by parent runbooks.  This runbook will recursively
 go through all sub directories from the root runbook path, starting with the most inner child folder, and publishes all child runbooks followed by its parent's runbooks.  


This runbook has a dependency on Connect-Azure, which you can download from     http://gallery.technet.microsoft.com/scriptcenter/Connect-to-an-Azure-f27a81bb.  The Azure-Connect runbook must be published
 for this runbook to run correctly.


**Requirements**


Before running this runbook, make sure the following components are available:


  *  VSO Git repository containing Azure Automation runbooks (ps1 files)

  *  VSO Alternate Authentication Credential for connecting to VSO-Git repository, configured from VSO dashboard (from 'My Profile')

  *  Automation Credential Asset containing the VSO Alternate Authentication Credentials

  *  Automation Account where the runbooks should be synced to

  *  Automation Certificate Asset containing the management certificate loaded to Azure

  *  Automation Connection Asset of type Azure, containing the subscription id and name of the certificate asset.  This is used for the runbook to connect to the Azure Automation Account.


**Runbook Contents**


The runbook's content are displayed below:

 

        
    
TechNet gallery is retiring! This script was migrated from TechNet script center to GitHub by Microsoft Azure Automation product group. All the Script Center fields like Rating, RatingCount and DownloadCount have been carried over to Github as-is for the migrated scripts only. Note : The Script Center fields will not be applicable for the new repositories created in Github & hence those fields will not show up for new Github repositories.
