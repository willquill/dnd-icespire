# How to use this repo for your own DnD campaign

Built using the amazing [MkDocs](https://www.mkdocs.org)

### Recommended tools:

- [VSCode](https://code.visualstudio.com/Download) for editing files
- Bash shell ([WSL2 if Windows](https://docs.microsoft.com/en-us/windows/wsl/install-win10))

### Clone the repo
```git clone https://github.com/willquill/dnd-icespire.git```

### Modify files
Modify mkdocs.yml to reflect your own site_name, pages, and theme.

### Build
```mkdocs build```

### Test
```mkdocs serve```

Visit http://127.0.0.1:8000 in your browser to see it in action.

Wanna know what's _really_ cool? You can edit your files on the fly and see the effect while ```mkdocs serve``` is active.

### Deploy

1. Put your Github private SSH key into ~/.ssh

For example, I'm using id_rsa_willquill

```chmod 600 ~/.ssh/id_rsa_willquill```

2. Create ~/.ssh/config file and put in these contents but customized for you:

```Host github-as-willquill
    HostName github.com
    User git
    IdentityFile ~/.ssh/id_rsa_willquill
    IdentitiesOnly yes
```

3. Create your own repo on Github.

4. Add the remote repo using the Host name from the config file above and use youruser/yourrepo.git:

```git remote add origin git@github-as-willquill:willquill/dnd-icespire.git
```

5. If you've enabled e-mail privacy in Github:

- Go to the Github Emails page [here](https://github.com/settings/emails)

- Copy the Github-provided email on that page and paste the following into your terminal:

git config user.email theid+youruser@users.noreply.github.com

More info [here](https://stackoverflow.com/questions/43378060/meaning-of-the-github-message-push-declined-due-to-email-privacy-restrictions)

4. Deploy
```mkdocs gh-deploy```
