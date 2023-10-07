# Zsh 
Add Oh My Zsh! with Autocompletion and Suggestions

What you will get:

#### Suggestions

![image](https://github.com/felipezarco/zsh/assets/11004919/0d32cec6-0d7e-4d36-b4ae-becc776d16c3)
**TIP**: Press arrow right to accept suggestions

#### Tab Finder

![image](https://github.com/felipezarco/zsh/assets/11004919/84634cfb-9e18-4836-96ac-6265a254fee9)
**TIP**: Type cd and then TAB across files

#### Syntax Highlight

![image](https://github.com/felipezarco/zsh/assets/11004919/13c1f4e0-b1c7-4293-9467-759e4f160f44)


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

![image](https://github.com/felipezarco/zsh/assets/11004919/4e906837-9b55-47da-b519-1cb777ae28b0)

**8 - Apply Changes**
```shell
source ~/.zshrc
```
