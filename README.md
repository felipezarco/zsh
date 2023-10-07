# Zsh 
Add Oh My Zsh! with Autocompletion and Suggestions

### 1 - Install Oh My Zsh!
```shell
sudo apt-get install zsh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

### 2 - Install Zsh Syntax Highlight
```shell
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git
echo "source ${(q-)PWD}/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh" >> ${ZDOTDIR:-$HOME}/.zshrc
source ./zsh-syntax-highlighting/zsh-syntax-highlighting.zsh
```

### 3 - Install Auto Suggestions
```shell
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```

### 4 - Install Fuzzy Finder 
```shell
git clone --depth 1 https://github.com/junegunn/fzf.git ~/.fzf && ~/.fzf/install
```

### 5 - Now, add the 3 and 4 plugins to your terminal
```
nano ~/.zshrc

```
**Find this line**: 

![image](https://github.com/felipezarco/zsh/assets/11004919/1f700505-f6a9-4a8f-967e-c42dfda2e4c5)

Replace 
```shell
plugins=(git)
```
With:
```shell
plugins=(
  git
  zsh-syntax-highlighting
  zsh-autosuggestions
  fzf
)
```
(or just add them in case you already oher plugins)

### 6 - Install Fira Code Font
```shell
sudo apt install fonts-firacode
```

Set this on your settings JSON VSCode file:
```json
"editor.fontFamily": "'Fira Code'",
"editor.fontLigatures": true
```

### 7 - Add alias to your favorite text editor

For example, open `code-insiders` with command `code`

**Open again the profile file with:**
```shell
nano ~/.zshrc
```
**Find these lines:**

![image](https://github.com/felipezarco/zsh/assets/11004919/27ecdbd1-64c7-4b7a-b3e0-3b10c8c14ba6)

**Add this uncommented line:** 
```shell
alias code='code-insiders' 
```
So that you have:

![image](https://github.com/felipezarco/zsh/assets/11004919/221ea4bd-36b2-44f3-a449-aadf31573059)

**8 - Apply Changes**
```shell
source ~/.zshrc
```
