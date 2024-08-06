In order for this type of script to work, you first need to create the app within your Azure tenant.

From portal.azure.com, go to App Registrations and create a new app. With your app created there are only two things you'll need to do.
 1. Generate Client Secret from Certificates & Secrets - save this, you'll need it later
 2. Edit API Permission so the app has permission to these
    Mail.Send
    User.Read
    User.ReadBasic.All
Now head over to the Overview tab to get all your apps info - App ID, Directory (tenant) ID, and your previously generated Client Secret - plug those into these variables
client_id = ''
client_secret = ''
tenant_id = ''

Once you have that, edit the list of servers/computers (you can use IP's as well).

Now edit these variables, please the mail_url email with a licensed user within your Azure tenant
    mail_url = 'https://graph.microsoft.com/v1.0/users/email@email.com/sendMail'
    sender_email = ""
    recipient_email = ""

  If you get errors check the following
    1. double check secrets/ID variables are correct
    2. ensure sender_email is a licensed user
    3. double check API Permissions
    ![image](https://github.com/user-attachments/assets/70648863-63dd-4ea8-bdb8-e7b65c8644a1)
    
