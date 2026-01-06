Kerberos authentication is the default authentication protocol for any recent version of Windows. Users who log into a service using Kerberos will be assigned tickets. Think of tickets as proof of a previous authentication. Users with tickets can present them to a service to demonstrate they have already authenticated into the network before and are therefore enabled to use it.

<img width="1047" height="416" alt="image" src="https://github.com/user-attachments/assets/d423900a-1b71-44dd-a22c-ed41f6806490" />

The client derives a User Key from its password and uses it to encrypt the username and a timestamp, then sends an Authentication Service Request (AS-REQ) to the KDC.

The KDC uses the User Key stored in Active Directory to decrypt the request. If the authentication is successful, the KDC generates a random Session Key, then creates a Ticket Granting Ticket (TGT) containing the Session Key and user information, and encrypts the TGT using the krbtgt key.

Finally, the KDC encrypts the Session Key with the User Key and sends both the TGT and the encrypted Session Key back to the client.

After receiving the TGT and the Session Key, the client no longer uses the password and instead uses the Session Key to authenticate to the KDC. When the client wants to access a service, it creates an Authenticator containing the username and a timestamp, encrypted with the Session Key, and sends the TGT, the Authenticator, and the SPN to the KDC to request a TGS. The KDC decrypts the TGT using the krbtgt key to retrieve the Session Key, then uses that Session Key to decrypt and validate the Authenticator. If the validation succeeds, the KDC confirms that the client is the legitimate owner of the TGT and issues the service ticket.
