# Lync User Manager
=================
The Lync Control panel is great for general user management BUT..
it has limitations. Some of these I come across regularly are as follows:-

  *  Private numbers are added from the Management Shell ONLY 
  *  Can’t set a PIN as you create the user in one step 
  *  Voice mail\Unified Messaging requires a trip to the Exchange servers 
  *  Voice mail and Unified Messaging in Office 365.. that’s another story 
  *  No way to compare or match users common attributes such as the numerous policies etc.

  *  Seen those pesky “Insufficient access rights to perform the operation” errors in the control panel?

## Functionality

Lync User Manager offers a single window to take care of Lync and Unified Messaging Moves, Adds, Changes and Deletions. Add to that the ability to compare users side-by-side AND even match and save to “copy” another users policies.

![002](https://user-images.githubusercontent.com/51378700/91380110-489a1b00-e878-11ea-8f5f-4fe9e083aedb.jpg)

### Connect

1. Launch Lync User Manager 
2. Fill in your AD, Exchange and Lync Server connection details. Remote PS sessions will be fired off to these in the background.
3. Click "Connect"
4. You will be presented with a credentials window to authenticate your admin account against AD, Exchange and Lync.
#### TIP
Watch the status change from ***Not Connected*** to **
*Connected* **as the different modules are loaded.
5. Once the connection is completed the User panes becomes active. This means we are ready to start managing our Lync users.

### Adding a new SFB\Lync user
**NOTE** Currently, the AD user needs to already exist. I may include this in vNext based on demand.

1. To add a new Lync user, fill in the user name in the user name box (you could click "Find"to make sure the user doesn’t exist).
2. Fill in the user details as you skip through the **Personal Attributes**,
**Common Attributes** and **UM Attributes**.
3. Once completed, click "Add"

### Change an existing user

  1. Fill in the User Name in the User Name box (either User 1 or User 2 panes can be used – makes no difference at all).

  2. Click "Connect", the user details will populate the boxes defining the users current setup. 
  #### TIP
  If no data is returned then the user does not exist as a SFB\Lync\UM user (yet).

  3. Make changes to the data in the boxes as required and click  "Change"
  
  *  To check that the changes have been made click "Find" to re-populate the results boxes. (it may take a few seconds for the changes to reflect so do be patient)

### Changing (Adding\Removing or Changing) Line URI

You could also simply add or remove a Line URI to the Line URI and Private Line URI boxes followed by "Change"

### Setting a PIN

Type in a PIN in the PIN box, check the Set PIN check box and click "Change" to commit the new PIN

### Copy User

Copy user is perhaps my favorite function. You can use copy both when adding **
new** or when **changing** an existing user.

### Copy to Add new user

  1. Find a template user in User 2 pane 
  2. Add a new user in the User 1 pane by copying the common attributes click "Copy"
  3. Fill in the Personal and UM attributes and click "Add"

#### Check your work, click "Find" to see your new user details.

### Copy to Change a user to match another

  1. Find the Template user in the User 1 pane (Remember that the 2 pains are totally interchangeable)
  2. Find the User to change in the User 2 pane. Click the "Copy" button in the User 2 pane so that the common attributes and UM Policy of User 2 now mirror that of User 1. 
  3. Click on the "Change" button in the User 2 Pane to commit the change 
  4. Check your work using "Find"

### Delete User

  1. Type the user name in the user name box and click "Find"
  2. Click "Delete" to delete BOTH the Lync User and the UM user details.
    *  You will be prompted to disable the UM mailbox
#### TIP If you intend to only delete UM, use the Disable UM Buttons. You will be prompted to confirm

## Pre-requisites

Powershell 3.0
For the Office 365 Powershell connection you will need:
  *  Install  .NET Framework 3.51 feature 
  *  After you install .NET Framework 3.51 get the latest updates 
  *  Install the [Microsoft Online Services Sign-In assistant](http://go.microsoft.com/fwlink/p/?linkid=236297)
  *  Install the [Windows Azure Active Directory (Azure AD) module](http://go.microsoft.com/fwlink/p/?linkid=236297) for the appropriate version of your operating system.

## Version History

V1.0.0.1 – First release
V1.1 – Introduced Hosted UM Policy selection
V1.1.0.1 – Added connect to Office 365 for UM in the cloud
V1.1.0.3 – Bug fixes and small UI updates

### Note
Only tested against Lync 2013
Tested from the following Operating Systems:-

  *  Windows 8.1 
  *  Windows Server 2008 
  *  Windows Server 2008 R2 
  *  Windows Server 2012 
  *  Windows Server 2012 R2 

And of course, this tool can be run remotely (RSAT may be required in some scenarios)


Please let me know of any bugs as well as suggestions.
     
    
