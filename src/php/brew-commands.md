# Useful Commands

1. **Installation and Updates:**
   - `brew install <package>`: Installs the specified package.
   - `brew uninstall <package>`: Uninstalls the specified package.
   - `brew upgrade`: Upgrades all installed packages to their latest versions.
   - `brew update`: Updates the Homebrew formulae and package lists.
   - `brew outdated`: Lists installed packages that have newer versions available.
   - `brew cleanup`: Removes old versions of installed packages and clears cache.

2. **Package Information and Management:**
   - `brew info <package>`: Displays information about the specified package.
   - `brew list`: Lists all installed packages.
   - `brew search <keyword>`: Searches for packages based on the provided keyword.
   - `brew deps <package>`: Lists the dependencies of the specified package.
   - `brew edit <package>`: Opens the formula for editing in the default text editor.

3. **Taps and Repositories:**
   - `brew tap <user/repo>`: Adds a new repository (tap) to Homebrew, allowing you to install packages from that repository.
   - `brew untap <user/repo>`: Removes a tap from Homebrew.

4. **Diagnostic and Troubleshooting:**
   - `brew doctor`: Diagnoses common issues and provides suggestions for fixing them.
   - `brew missing`: Lists packages that are missing their dependencies.

5. **Version Control:**
   - `brew switch <package> <version>`: Switches to a specific version of a package.
   - `brew pin <package>`: Prevents a package from being upgraded when running `brew upgrade`.

6. **Casks (Graphical Applications):**
   - Homebrew Cask is an extension that allows you to install macOS applications and large binaries.
   - `brew cask install <app>`: Installs a macOS application.
   - `brew cask uninstall <app>`: Uninstalls a macOS application.

These commands provide a good starting point for using Homebrew effectively. Remember that you can always refer to Homebrew's official documentation or run `brew help` to get more information about available commands and their usage. The Homebrew ecosystem is actively maintained and expanded upon by the community, so staying up to date with any changes or new features is beneficial.
