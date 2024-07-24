# Cool-One-Liners
A personal compilation of cool one(-ish) liners. Perhaps they will have a better resting place in the future.

# fzf
fzf is super cool. It is a very well loved program, and even then I think it's serverly underrated.

## Selectively remove orphaned dependencies on arch
1. `sudo zsh -c "pacman -Qqdt | fzf --multi --preview 'pacman -Qi {}' --reverse | pacman -Rns -"` to start fzf listing orphaned deps with a preveiw
2. Select the packages to remove with tab and remove them with enter (we could use `--bind` here, but that only works for the currently selected item unless I missed something)
3. `sudo zsh -c "pacman -Qqdt | sudo pacman -D --asexplicit -"` to mark any remaining packages you want to keep as explicit
