# Fix: VSCode Not Recognizing Standard Shell Change

## Steps to Resolve:

1. Open **VSCode**.
2. Press **CMD + SHIFT + P** to open the Command Palette.
3. Type and select **"Preferences: Open Settings (JSON)"**.
4. In the `settings.json` file, search for `"terminal.integrated.profiles.osx"`.
   - If the entry doesn't exist, you can add it manually.
5. Add the following code to configure your shell (replace `${YOU_BASH_LOCATION}` with the actual path to your bash):

   ```json
   "terminal.integrated.profiles.osx": {
       "bash": {
           "path": "${YOU_BASH_LOCATION}",
           "args": [
               "-i"  // Ensure this is -i, not -l
           ],
           "icon": "terminal-bash"
       }
   }
