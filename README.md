If after installing nvm and node by running:

```
>>> nvm install node
```

the command

```
>>> node -v
```

returns an old version of node when you close the terminal, and when you re-run

```
>>> nvm install node
```

it returns a version that's already installed, it means node is bugged.  
To fix this, follow these instructions:

1. Close every currently open terminal.
2. Open a terminal with the bugged version of Node.
3. Run:
    ```
    >>> which node
    ```
4. Copy the path printed in the terminal and modify the string by removing the end of the path, which will look something like "/bin/node". The last folder in the path should be the bugged version of Node.
5. Save the modified path:
    ```
    >>> my_path=[the modified string]
    ```
6. Run:
    ```
    >>> nvm install node
    ```
7. Run:
    ```
    >>> nvm alias default [your_version]
    ```
   where `your_version` is the version printed in the terminal after the previous step.
8. Run:
    ```
    >>> sudo rm $my_path -r
    ```
9. Type in your password.
10. Enjoy!

This should render properly in any Markdown-supported platform. Let me know if you'd like any more tweaks!
