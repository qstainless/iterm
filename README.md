iTerm2
-
My [iTerm2](https://www.iterm2.com/) profile settings.

To install the matrix theme, create a folder to save the theme file in this repo. I have not made any changes to the theme file, but you can find the original [here](https://gist.github.com/rdempsey/596193b8ede69767719c#file-matrix_color_scheme_iterm2).
 
In terminal, cd to that folder. Then, copy, paste and run the following code:
```
for f in *; do
THEME=$(basename "$f")
defaults write -app iTerm 'Custom Color Presets' -dict-add "$THEME" "$(cat "$f")"
done
```

Finally, in iTerm2, go to Preferences->Profiles->Colors. Click the `Color Presets...` dropdown and select `matrix_color_scheme_iterm2`.

Or you can simply import my profile and make it your own (or whatever):
1. Go to Preferences->General. You will see the following at the bottom of the panel:
![alt text](https://github.com/qstainless/iterm/blob/master/iTerm2-preferences.png "iTerm2 Preferences Pane")

2. Check `Load preferences from a custom folder or URL:`
3. Browse for the folder where you want to save your custom profile. If you are like me and have Dropbox installed, save it to a Dropbox folder. This will allow you to have the exact same settings on different computers.
4. Check `Save changes to folder when iTerm2 quits`.
5. Click `Save Current Settings to Folder`.

And you're all set!

See my oh-my-zsh custom settings [here](https://github.com/qstainless/dotfiles/blob/master/.zshrc).