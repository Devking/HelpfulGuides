Use [`nvm`](https://github.com/nvm-sh/nvm) for Node version management.

```
# Install nvm
brew upgrade
brew install nvm

# Install the latest version of node
nvm install node

# Install a specific version of node
nvm install 10.10.0

# List the installed versions of node
nvm ls

# Use the latest version of node
nvm use node

# Use a specific version of node
nvm use 10.10.0
```

Git init.

Install the necessary packages using `npm`.

```
# Create package.json which tracks dependencies
npm init

# Install the Express package and save it in the dependencies list
npm install express --save
```

For your `.gitignore`:

```
node_modules/
package-lock.json
```
