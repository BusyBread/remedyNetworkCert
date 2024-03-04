# remedyNetworkCert
remedyNetworkCert is a Jamf Pro workflow that allows network/computer certificates to be re-issued from Self-Service.

# Requirements
1. swiftDialog (at least version 2.3.2)
2. API Client with the following privileges:
    * Read Static Computer Groups
    * Update Static Computer Groups
3. A static computer group in Jamf Pro (note the ID in the URL)
4. UUID of the network configuration profile

# Deployment
1. Download the remedyNetworkCert.zsh script.
2. Create a new script in **Jamf Pro > Settings > Computer Management > Scripts** and add the following parameter labels to the newly added script:
    * Client ID
    * Client Secret
    * Static group ID
    * Network profile UUID
3. Create a new policy in **Jamf Pro > Computers > Policies > New**:
    * Set the `Execution Frequency` to `Ongoing`
    * Add the remedyNetworkCert.zsh as the script payload and provide the parameters.
    * Enable Self-Service and add description letting the user know they need to be on VPN to complete this.
    * Scope to `All Computers`
