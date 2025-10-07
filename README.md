**1. Dependencies:**
 
 - yay:

       yay -S pfetch zsh
   
* If you dont have yay installed, [Click me](https://github.com/Jguer/yay) after you followed this guide you can delete the yay folder
  
  - Or just run this(thats from the website)
    
             sudo pacman -S --needed git base-devel && git clone https://aur.archlinux.org/yay.git && cd yay && makepkg -si

<br/>

**2.Now clone the repos:**

 - my repo
    
       git clone https://github.com/Jona1302/My-Dotfiles.git

- oh-my-zsh
     
      sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
       
- powerlevel10k

      git clone --depth=1 https://github.com/romkatv/powerlevel10k.git "${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k"

<br>

**3. Now we have to remove the existing files:**

       rm -rf ~/.config/kitty \
              ~/.zshrc \
              ~/.p10k.zsh    
 
<br>
<br>

**4. Now we can move the new files to the .Config directory**

!!!MAKE SURE THAT YOU ARE IN THE (MY-DOTFILES) DIRECTORY!!!

         cp -r kitty/ ~/.config
         cp .p10k.zsh .zshrc ~/


**5. Last but no least we have to chainge the shell from bash to zsh by running:**

- change shell

      chsh -s $(which zsh)

- change shell(for root)

      sudo chsh -s $(which zsh)


