# Connecting to GitHub using HTTPS

When you are prompted to authenticate will depend on whether you have cloned a public or private repository. This will happen immediately when trying to clone a private repository, or the first time you push if a public repository.

1.	In Git Bash or RStudio, clone a repository from GitHub using the HTTPS URL.

2.  A GitHub window will pop up to prompt you to authenticate. (Note: This may appear behind your open Git Bash or RStudio window.) Click the blue button to 'Sign in with your browser'. You will be directed to a browser window.

    <img width="315" alt="" src="https://github.com/user-attachments/assets/930d4f53-2805-4448-82b3-0fa76d13d445" />

3.  If it is your first time using HTTPS, you may see a page asking you to 'Authorize Git Credential Manager'. If so, click the green button to 'Authorize git-ecosystem'.

    <img width="315" alt="" src="https://github.com/user-attachments/assets/62ab04c6-d201-4bb7-b044-807bc8902095" />

4.  You will then be prompted to login to your GitHub account (if you aren't already logged in). 

    It might be unclear when authentication has been successful. You may see a 'Can't reach this page' error, however if you navigate back to Git Bash or RStudio, you should see that authentication has completed. 

You are now set up to use HTTPS to connect to GitHub.

## Notes

* After successful authentication, you can view, edit or delete your credentials in Windows Credential Manager. You can find this in Control Panel > Credential Manager > Windows Credentials. Under 'Generic Credentials', you should see an entry for `git:https://github.com`.

* If you change your GitHub log-in details and authentication fails, delete your details from Windows Credential Manager and repeat the steps above.

* If the GitHub authentication window is closed or authentication is unsuccessful, then you may see another prompt asking you to enter your GitHub username and then password. You may also be prompted to enter these details within Git Bash. However, [this method is no longer accepted form of authentication](https://github.blog/security/application-security/token-authentication-requirements-for-git-operations/), and so will fail.

* The GitHub pop-up window also provides options to authenticate by signing in with a code, or by providing a Personal Access Token (PAT). These are equally valid methods.

* If, for whatever reason, you would like to revoke authorisation of Git Credential Manager, this can be done on GitHub via: Settings > Applications > Authorized OAuth Apps.
