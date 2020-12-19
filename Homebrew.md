# We'll be installing Homebrew in the /opt directory.
cd /opt

# Create a directory for Homebrew. This requires root permissions.
sudo mkdir homebrew

# Make us the owner of the directory so that we no longer require root permissions.
sudo chown -R $(whoami) /opt/homebrew

# Download and unzip Homebrew. This command can be found at https://docs.brew.sh/Installation.
curl -L https://github.com/Homebrew/brew/tarball/master | tar xz --strip 1 -C homebrew

# Add the Homebrew bin directory to the PATH. If you don't use zsh, you'll need to do this yourself.
echo "export PATH=/opt/homebrew/bin:$PATH" >> ~/.zshrc