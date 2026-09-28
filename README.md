# server-keys

Who can SSH into which of my servers, as which account. Servers read
[`keytree.yaml`](keytree.yaml) hourly with [keytree](https://github.com/ragibkl/keytree).

Install on a new server (as root):

```sh
wget -qO- https://ragibkl.github.io/keytree/install | sh -s https://raw.githubusercontent.com/ragibkl/server-keys/main/keytree.yaml
```

- **New laptop**: add its key to GitHub. Nothing to change here.
- **Give someone access**: add them under `users`, then to a group or a
  server's list. Open a PR.
- **Remove access**: delete them from the lists.
- **Preview a change**: `keytree plan --name <server> keytree.yaml`.

Whoever can push to `main` controls access to every server: keep `main`
protected.
