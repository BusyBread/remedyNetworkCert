# remedyNetworkCert
remedyNetworkCert is a Jamf Pro workflow that allows network certificates to be re-issued from Self-Service.

## Requirements
1. API Client with the following privileges:
    * Read Static Computer Groups
    * Update Static Computer Groups
2. A static computer group in Jamf Pro (note the ID in the URL)
    * https://JAMF_PRO/staticComputerGroups.html?**id=907**
