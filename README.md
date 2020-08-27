Lync User Manager
=================

            

The Lync Control panel is great for general user management BUT..


it has limitations. Some of these I come across regularly are as follows:-


  *  Private numbers are added from the Management Shell ONLY 
  *  Can’t set a PIN as you create the user in one step 
  *  Voice mail\Unified Messaging requires a trip to the Exchange servers 
  *  Voice mail and Unified Messaging in Office 365.. that’s another story 
  *  No way to compare or match users common attributes such as the numerous policies etc.

  *  Seen those pesky “Insufficient access rights to perform the operation” errors in the control panel?

Functionality

Lync User Manager offers a single window to take care of Lync and Unified Messaging Moves, Adds, Changes and Deletions. Add to that the ability to compare users side-by-side AND even match and save to “copy” another users policies.


![Image](https://github.com/PaulB-NZ/lync-user-manager/raw/master/001.jpg)


  *  Launch Lync User Manager 
  *  Fill in your AD, Exchange and Lync Server connection details. Remote PS sessions will be fired off to these in the background.


![Image](https://github.com/PaulB-NZ/lync-user-manager/raw/master/002.jpg)


4. Click ![Image](https://github.com/PaulB-NZ/lync-user-manager/raw/master/011.jpg)


5. You will be presented with a credentials window to authenticate your admin account against AD, Exchange and Lync.


![Image](https://github.com/PaulB-NZ/lync-user-manager/raw/master/001.jpg)


Watch the status change from ***Not Connected*** to **
*Connected* **as the different modules are loaded.


![Image](https://github.com/PaulB-NZ/lync-user-manager/raw/master/006.jpg)
6. Once the connection is completed the User panes becomes active. This means we are ready to start managing our Lync users.

Adding a new Lync user

**NOTE** Currently, the AD user needs to already exist. I may include this in vNext based on demand.


1. To add a new Lync user, fill in the user name in the user name box (you could click
![Image](https://github.com/PaulB-NZ/lync-user-manager/raw/master/010.jpg)to make sure the user doesn’t exist).


![Image](https://github.com/PaulB-NZ/lync-user-manager/raw/master/007.jpg)


2. Fill in the user details as you skip through the **Personal Attributes**,
**Common Attributes** and **UM Attributes**.


![Image](https://github.com/PaulB-NZ/lync-user-manager/raw/master/002.jpg)


3. Once completed, click 
![Image](https://github.com/PaulB-NZ/lync-user-manager/raw/master/013.jpg) to send the request to the servers. Wait a few seconds and click
![Image](https://github.com/PaulB-NZ/lync-user-manager/raw/master/010.jpg) to confirm that the user has been created as expected.

Change an existing user

  *   Fill in the User Name in the User Name box (either User 1 or User 2 panes can be used – makes no difference at all).

  *  Click ![Image](https://github.com/PaulB-NZ/lync-user-manager/raw/master/010.jpg), the user details will populate the boxes defining the
 users current setup. **TIP** If no data is returned then the user does not exist as a Lync\UM user (yet).

  *  Make changes to the data in the boxes as required and click 
![Image](https://github.com/PaulB-NZ/lync-user-manager/raw/master/014.jpg) to commit the changes.

  *  To check that the changes have been made click 
![Image](https://github.com/PaulB-NZ/lync-user-manager/raw/master/010.jpg) to re-populate the results boxes. (it may take a few seconds for the changes to reflect so do be patient)

Changing (Adding\Removing or Changing) Line URI<\h2>

You could also simply add or remove a Line URI to the Line URI and Private Line URI boxes followed by
![Image](https://github.com/PaulB-NZ/lync-user-manager/raw/master/014.jpg) to commit.

Setting a PIN

Type in a PIN in the PIN box, check the Set PIN check box and click 
![Image](https://github.com/PaulB-NZ/lync-user-manager/raw/master/014.jpg) to commit the new PIN

Copy User

Copy user is perhaps my favorite function. You can use copy both when adding **
new** or when **changing** an existing user.

Copy to Add new

  *  Find a template user in User 2 pane 
  *  Add a new user in the User 1 pane by copying the common attributes 
![Image](https://github.com/PaulB-NZ/lync-user-manager/raw/master/015.jpg)

  *  Fill in the Personal and UM attributes and click 
![Image](https://github.com/PaulB-NZ/lync-user-manager/raw/master/013.jpg)

  *  Check your work, click 
![Image](https://github.com/PaulB-NZ/lync-user-manager/raw/master/010.jpg) to see your new user details.

Copy to Change a user to match another

  *  Find the Template user in the User 1 pane (Remember that the 2 pains are totally interchangeable)

  *  Find the User to change in the User 2 pane. 
  *  Click the ![Image](https://github.com/PaulB-NZ/lync-user-manager/raw/master/015.jpg) button in the User 2 pane so that the common
 attributes and UM Policy of User 2 now mirror that of User 1. 
  *  Click on the ![Image](https://github.com/PaulB-NZ/lync-user-manager/raw/master/014.jpg) button in the User 2 Pane to commit the
 change 
  *  Check your work using 
![Image](https://github.com/PaulB-NZ/lync-user-manager/raw/master/010.jpg)

Delete User

  *  Type the user name in the user name box and click 
![Image](https://github.com/PaulB-NZ/lync-user-manager/raw/master/010.jpg)

  *  Click ![Image](https://github.com/PaulB-NZ/lync-user-manager/raw/master/016.jpg) to delete BOTH the Lync User and the UM user details.

  *  You will be prompted to disable the UM mailbox![Image](https://github.com/PaulB-NZ/lync-user-manager/raw/master/017.jpg)


**TIP** If you intend to only delete UM, use the Disable UM Buttons. You will be prompted to confirm


Download

Pre-requisites

Powershell 3.0


Fot the Office 365 Powershell connection you will need:












  *  Install  .NET Framework 3.51 feature 
  *  After you install .NET Framework 3.51 get the latest updates 
  *  Install the [Microsoft Online Services Sign-In assistant](http://go.microsoft.com/fwlink/p/?linkid=236297)

  *  Install the [Windows Azure Active Directory (Azure AD) module](http://go.microsoft.com/fwlink/p/?linkid=236297) for the appropriate version of your operating system.











Version History

V1.0.0.1 – First release


V1.1 – Introduced Hosted UM Policy selection


V1.1.0.1 – Added connect to Office 365 for UM in the cloud


V1.1.0.3 – Bug fixes and small UI updates


**Future releases**


vNext – Manage Lync users in O365


Only tested against Lync 2013
Tested from the following Operating Systems:-


  *  Windows 8.1 
  *  Windows Server 2008 
  *  Windows Server 2008 R2 
  *  Windows Server 2012 
  *  Windows Server 2012 R2 

And of course, this tool can be run remotely (RSAT may be required in some scenarios)


Please let me know of any bugs as well as suggestions.


        
    
