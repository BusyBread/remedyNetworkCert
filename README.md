# remedyNetworkCert
remedyNetworkCert is a Jamf Pro workflow that allows network certificates to be re-issued from Self-Service.

# Requirements
1. API Client with the following privileges:
    * Read Static Computer Groups
    * Update Static Computer Groups
2. A static computer group in Jamf Pro (note the ID in the URL)
    * https://JAMF_PRO/staticComputerGroups.html?**id=907**
3. UUID of the network configuration profile

# Deployment
1. Download the remedyNetworkCert.zsh script.
2. Create a new script in Jamf Pro > Settings > Computer Management > Scripts and ddd the following parameter labels to the newly added script:
    4. Client ID
    5. Client Secret
    6. Static group ID
    7. Network profile UUID
3. Create a new policy in Jamf Pro > Computers > Policies > New
    1. Set the `Execution Frequency` to `Ongoing`
    1. Add the remedyNetworkCert.zsh as the script payload and provide the parameters.
    2. Add Self-Service entry with description letting the user know they need to be on VPN to complete this.
