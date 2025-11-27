# Webdev 101

Basic instructions for maintaining this site.

## Requirements for local testing on APT based systems (Ubuntu etc.)

This is an educated guess and may not work for every machine.

```sh
# Update package list
sudo apt update

# Install Ruby and build tools
sudo apt install ruby-full build-essential zlib1g-dev -y

# Add Ruby to PATH (assuming you're using bash)
echo 'export GEM_HOME="$HOME/gems"' >> ~/.bashrc
echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc

# Install Bundler and Jekyll
gem install bundler jekyll
```

## Testing locally on WSL

```sh
jekyll serve --host 0.0.0.0 --port 8000 --livereload
```

On a successful build, the website should be available at <http://localhost:8000/>

## Recommended tooling

YAML (.yml)

- [yamllint](https://yamllint.readthedocs.io/en/stable/)
- [VS Code: Linter](https://marketplace.visualstudio.com/items?itemName=fnando.linter)
