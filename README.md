Настройка новой системы.
SCALE:        way-displays (swaymsg -t get_outputs)
resolv.conf:  настроить DNS в NetworkManager 8.8.8.8 и 8.8.4.4
helix:        https://github.com/estin/simple-completion-language-server
yazi:         https://yazi-rs.github.io/docs/configuration/overview


#Configure zsh prompt with p10k
i had the same error “p10k configure: cannot create /usr/share/zsh/p10k.zsh because /usr/share/zsh is readonly” when it tried to configure powerlevel10k.
what i did was, open /usr/share/zsh/manjaro-zsh-prompt
look for (line 15):
[[ ! -f /usr/share/zsh/p10k.zsh ]] || source /usr/share/zsh/p10k.zsh
change it into:
# [[ ! -f /usr/share/zsh/p10k.zsh ]] || source /usr/share/zsh/p10k.zsh
then save manjaro-zsh-prompt, open your konsole and it will prompt to configure powerlevel10k. this will create a .p10k.zsh file in your home directory and modify your .zshrc
if you need to make changes, you can now use “p10k configure”
if you like to use the stock config of manjaro-zsh-config, copy /usr/share/zsh/p10k.zsh file to you home directory, replacing .p10k.zsh
