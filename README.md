# Github CI-CD for common projects

# SSH

```
ssh-keygen -m PEM -t rsa -b 4096
```

**Please Note:** You should not set a Passphrase (keep it empty) for the private key you generated. Because rsync ssh (used for deploy) does not support private key password to be entered as a command line parameter.

# Get start
Those configurations are for sending files only though ssh and rsync, 
if you want to build only through Github use **build.yml**, it will build and send new build files

**Make sure to not change production branch**

# NodeJS

- Copy ecosystem.config.js to the root of the project (it will be used to serve the project using pm2) and change the app name to the repo name (No need for nextjs)
- Make sure that .env is included in .gitignore (otherwise it will be rewritten in the production server)

# Laravel

- If there is any commands that should be included in the build steps, then you can add them after **SCRIPT_AFTER: |** section.
