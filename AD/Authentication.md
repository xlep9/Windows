Kerberos authentication is the default authentication protocol for any recent version of Windows. Users who log into a service using Kerberos will be assigned tickets. Think of tickets as proof of a previous authentication. Users with tickets can present them to a service to demonstrate they have already authenticated into the network before and are therefore enabled to use it.

<img width="1047" height="416" alt="image" src="https://github.com/user-attachments/assets/d423900a-1b71-44dd-a22c-ed41f6806490" />

The client derives a User Key from its password and uses it to encrypt the username and a timestamp, then sends an Authentication Service Request (AS-REQ) to the KDC.

The KDC uses the User Key stored in Active Directory to decrypt the request. If the authentication is successful, the KDC generates a random Session Key, then creates a Ticket Granting Ticket (TGT) containing the Session Key and user information, and encrypts the TGT using the krbtgt key.

Finally, the KDC encrypts the Session Key with the User Key and sends both the TGT and the encrypted Session Key back to the client.

After receiving the TGT and the Session Key, the client no longer uses the password and instead uses the Session Key to authenticate to the KDC. When the client wants to access a service, it creates an Authenticator containing the username and a timestamp, encrypted with the Session Key, and sends the TGT, the Authenticator, and the SPN to the KDC to request a TGS. The KDC decrypts the TGT using the krbtgt key to retrieve the Session Key, then uses that Session Key to decrypt and validate the Authenticator. If the validation succeeds, the KDC confirms that the client is the legitimate owner of the TGT and issues the service ticket.

<img width="1049" height="486" alt="image" src="https://github.com/user-attachments/assets/fe570bc5-7d17-44c0-86cb-070d0d44c40b" />

As a result, the KDC will send us a TGS along with a Service Session Key, which we will need to authenticate to the service we want to access. The TGS is encrypted using a key derived from the Service Owner Hash. The Service Owner is the user or machine account that the service runs under. The TGS contains a copy of the Service Session Key on its encrypted contents so that the Service Owner can access it by decrypting the TGS.

<img width="1029" height="362" alt="image" src="https://github.com/user-attachments/assets/38cff3ce-2d4e-4706-90aa-e8e928c5e73a" />


The TGS can then be sent to the desired service to authenticate and establish a connection. The service will use its configured account's password hash to decrypt the TGS and validate the Service Session Key.

