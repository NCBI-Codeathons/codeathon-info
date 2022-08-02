# AWS quick start guide for NCBI codeathon participants

## Logging into AWS

Check the email account that you registered for the codeathon with for an email with subject line "NCBI Codeathon Credentials".
If you don't have one and it's not in spam, let us know.

Follow the link in the email or go to [https://codeathon.ncbi.nlm.nih.gov](https://codeathon.ncbi.nlm.nih.gov).
You will be prompted to sign in with the username and Password contained in the email.
After signing in, you will be prompted to choose a new password.

Once you've set your password, you will be prompted to selecet a role.
You should have only one role available: `NCBI-Codeathon-Participant-Role`.
Click "Sign-In" next to this role.
This will take you to the AWS Console Home

## Creating an EC2 instance

Once you've logged in to AWS, you can create an *EC2 instance*, that is a virtual machine, a computer in the cloud that you can log into for your analysis.
The following instructions will give you a general-purpose machine with 4 computing cores and 1TB of storage.
If you decide you need a more powerful or specialized virtual machine to do your analysis, we can help you set that up too.
We can also help you set up a Jupyter or RStudio server for your team.

In the search bar next to "Services" at the top of the page search for "EC2" and then select "EC2" in the results.

On the EC2 screen, select "Launch instance" and then "Launch instance from template".

On the launch screen, select the template we've set up for you.
Under "Source template", select "CodeathonQuickstart".

The next step is to generate a public/private key pair so that you can connect to the instance with ssh.
Under "Key pair (login)" select "Create new key pair".
Give your keypair a name that starts with `codeathon-`.
Put the downloaded private key file somewhere you'll be able to find it later (like in your `.ssh/` directory).

Next, name your instance. Under "Resource tags", click "Add tag", then type "Name" in the "Key" field and a name that starts with `codeathon-` in the "Value" field.

Now you're ready to launch the instance.
Scroll to the bottom of the page and click the "Launch instance" button.

## Connecting to the instance

There are two ways to connect to the instance you've just created:
either in your browser with EC2 Instance Connect or with an SSH client.
If you've never used SSH before, I recommend starting with Instance Connect.
If you're comfortable with SSH, that option will be more convenient.

After you've launched your instance, you should get a message indicating that the instance launched successfully.
Click the link in the message with the instance ID.
That link will take you to a list of EC2 instances that's filtered to only show the one you just created.
Check the checkbox next to the name of your instance.
Under the "Actions" dropdown menu select "Connect".

On the "Connect to instance" screen, you will have several options.
The default view lets you connect with EC2 Instance Connect, which will open a terminal emulator in your browser window.
If you'd like to use this option, select "Connect".

If you'd prefer to use an SSH client to connect, select "SSH client" and follow the instructions.
Use the key file you created when you launched the instance.
Be sure to run the `chmod 400` command on your private key file to set the correct permissions.
