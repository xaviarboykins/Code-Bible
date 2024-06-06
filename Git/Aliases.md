# Must Have Git Aliases

## Git Aliases for Enhanced Log Viewing

This guide provides handy Git aliases for listing commits in a concise and colorful format, with branch and tag annotations.

### Short Form Log with Colors and Annotations

You can list commits in a short form with colors and branch/tag annotations using the following alias:

### Alias Configuration

Add the following line to your `.gitconfig` file under the `[alias]` section:

```ini
[alias]
    ls = log --pretty=format:"%C(yellow)%h%Cred%d\\ %Creset%s%Cblue\\ [%cn]" --decorate
```

### Command Usage

Use the `git ls` command to view the commit log in short form:

```sh
git ls
```

### Example Output

The output will look something like this:

![git-ls](https://github.com/xaviarboykins/Code-Bible/assets/119615611/48dd0a8e-862f-4d59-8d96-1b79a5337ea7)

## Long Form Log with Changes

For a long log that includes changes, use the following alias:

### Alias Configuration

Add the following line to your `.gitconfig` file under the `[aliases]` section:

```ini
[alias]
    ll = log --pretty=format:"%C(yellow)%h%Cred%d\\ %Creset%s%Cblue\\ [%cn]" --decorate --numstat
```

### Command Usage

Use the `git ll` command to view the detailed commit log with changes:

```sh
git ll
```

### Explanation of Format

- `%C(yellow)%h`: Displays the commit hash in yellow.
- `%Cred%d\`: Displays branch or tag annotations in red.
- `%Creset%s`: Resets color and displays the commit message.
- `%Cblue\\ [%cn]`: Displays the committer name in blue.
- `--decorate`: Adds branch and tag names.
- `--numstat`: Shows the number of insertions and deletions for each commit (only in `git ll`).

By adding these aliases to your Git configuration, you can enhance your Git log viewing experience with colorful, annotated commit histories.




