# ubuntu
對我在我的虛擬機上的一些使用較友善的設定紀錄一下，有些是很久以前寫的，但我想應該都還能用

## ohMyZsh
[ohmyzsh](https://github.com/ohmyzsh/ohmyzsh)
讓你的terminal變得美美的工具，但是有些字體電腦沒有辦法幫你印出來QQ，舉例向下圖
![](https://i.imgur.com/mYoGgt8.png)
[網路上關於putty印不出字體的文章 + 解決方法](https://superuser.com/questions/393834/how-to-configure-putty-to-display-these-characters)

#### 解決辦法整理
- [下載這個字形](https://dejavu-fonts.github.io/)
- 解壓縮後，把下圖的幾個檔案複製到"C:\Windows\Fonts"這個位置
    - ![](https://i.imgur.com/fj9QBZN.png)
- 打開putty時選擇"DejaVu Sans Mono "這個字體


幸福就是這麼簡單
![](https://i.imgur.com/eVLouHf.png)

### oy-my-ZSH主題設定

```
# 有任何對shell的更動都要執行這個才看得到
exec $SHELL
```

[主題樣式一覽](https://github.com/ohmyzsh/ohmyzsh/wiki/Themes)
```
vim ~/.zshrc

找到ZSH_THEME
```

- agnoster(雖然超多人用但是我覺得沒有特別去設定字體的話這個在putty上面超級醜)
    - https://github.com/oh-my-fish/theme-agnoster/issues/46
    - 解決問題:[載這字體](https://github.com/powerline/fonts), [沒用的話用這個](https://github.com/powerline/fonts/tree/master/DejaVuSansMono)
    - 字體選這個：DejaVu Sans Mono for Powerline
    - [顏色處理](https://www.twblogs.net/a/5b829e8c2b717766a1e91acc)

### oh-my-zsh autosuggestion設定
[github](https://gist.github.com/dogrocker/1efb8fd9427779c827058f873b94df95)
#### 簡單整理
```
# 下載zsh-autosuggestions
git clone https://github.com/zsh-users/zsh-autosuggestions.git $ZSH_CUSTOM/plugins/zsh-autosuggestions

# 下載zsh-syntax-highting
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git $ZSH_CUSTOM/plugins/zsh-syntax-highlighting

vim ~/.zshrc
plugins=(git zsh-autosuggestions zsh-syntax-highlighting)
```

## .vimrc
### vim一些方便設定
[參考上面的vimrc.txt](https://github.com/yenchia189929/ubuntu/tree/main/settings)

[為什麼要學vim](https://medium.com/@jinghua.shih/每個開發者都應該要會用的編輯器-vim-5f83349973a3)
[vim plugin大集合](https://vimawesome.com)
### vim主題
[vim 主題設定教學](https://clay-atlas.com/blog/2020/05/04/vim-cn-note-scheme-colors-settings/)
```
# 以hybrid為範例
sudo mkdir ~/.vim/colors
git clone https://github.com/w0ng/vim-hybrid.git
sudo cp vim-hybrid/colors/hybrid.vim ~/.vim/colors/
sudo rm -rf vim-hybrid

# vimrc設定
syntax on
set t_Co=256
colorscheme hybrid
```
[colorsheme一覽](https://colorswat.ch/vim/list?cat=all)
我覺得[hybrid](https://github.com/w0ng/vim-hybrid)挺美ㄉ


