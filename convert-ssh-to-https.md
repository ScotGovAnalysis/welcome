# Converting existing cloned repositories to HTTPS

It is not necessary to re-clone repositories you have already cloned using SSH. To switch these to use an HTTPS connection, following these steps:

1.	Open Git Bash within your project directory. To do this, navigate to your project folder in File Explorer, right click and select "Open Git Bash here".

2.	Run the following code to view your current remote URL. If you are using SSH, the URL will start with `git@github.com:`.

    ```
    git remote get-url origin
    ```

3.	Run the following code in Git Bash to convert the URL from SSH to HTTPS:

    ```
    git remote set-url origin $(git remote get-url origin | sed 's_git@github.com:_https://github.com/_')
    ```

4.	To confirm this has worked, rerun the following code. The URL should now begin with `https://github.com/`.

    ```
    git remote get-url origin
    ```

Guidance is also available on [using HTTPS authentication for the first time](using-https.md).
