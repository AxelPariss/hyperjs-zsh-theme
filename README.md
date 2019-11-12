# Gorgeous Terminal : HyperJS + ZSH + powerlevel10k + plugins

<p align="center">
  <img src="https://github.com/AxelPariss/hyperjs-zsh-theme/blob/master/images/screen.jpg?raw=true" alt="Oh My Zsh">
</p>

## Étape 1 : Installez HyperJS

Installez le terminal [HyperJS](https://hyper.is/).

## Étape 2 : Installez ZSH

Installez ZSH :
```
brew install zsh
```

Définissez ZSH comme shell par défaut :
```
chsh -s $(which zsh)
```
## Étape 3 : Changez le thème de ZSH

Téléchargez le thème `powerlevel10k` :
```
git clone https://github.com/romkatv/powerlevel10k.git $ZSH_CUSTOM/themes/powerlevel10k
```

Modifiez `ZSH_THEME="powerlevel10k/powerlevel10k"` dans le fichier `~/.zshrc`.


## Étape 4 : Configurez HyperJS

Remplacez votre fichier `~/.hyper.js` par :
```js
// Future versions of Hyper may add additional config options,
// which will not automatically be merged into this file.
// See https://hyper.is#cfg for all currently supported options.


module.exports = {
  config: {    
    hyperline: {                                                            
      plugins: [                                                                 
        "ip",                                                                    
        "cpu",                                                                   
        "spotify",
        "battery",
        "memory"                                                               
      ]                                                                          
    },
    
    // or `'canary'` for less polished but more frequent updates
    updateChannel: 'canary',

    // default font size in pixels for all tabs
    fontSize: 26,

    // font family with optional fallbacks
    fontFamily: '"MesloLGS NF", monospace',
    // default font weight: 'normal' or 'bold'
    fontWeight: 'normal',

    // font weight for bold characters: 'normal' or 'bold'
    fontWeightBold: 'bold',

    // terminal cursor background color and opacity (hex, rgb, hsl, hsv, hwb or cmyk)
    cursorColor: 'rgba(248,28,229,0.8)',

    // terminal text color under BLOCK cursor
    cursorAccentColor: '#000',

    // `'BEAM'` for |, `'UNDERLINE'` for _, `'BLOCK'` for █
    cursorShape: 'BLOCK',

    // set to `true` (without backticks and without quotes) for blinking cursor
    cursorBlink: false,

    // color of the text
    foregroundColor: '#fff',

    // terminal background color
    // opacity is only supported on macOS
    backgroundColor: '#000',

    // terminal selection color
    selectionColor: 'rgba(248,28,229,0.3)',

    // border color (window, tabs)
    borderColor: '#333',

    // custom CSS to embed in the main window
    css: '',

    // custom CSS to embed in the terminal window
    termCSS: '',

    // if you're using a Linux setup which show native menus, set to false
    // default: `true` on Linux, `true` on Windows, ignored on macOS
    showHamburgerMenu: '',

    // set to `false` (without backticks and without quotes) if you want to hide the minimize, maximize and close buttons
    // additionally, set to `'left'` if you want them on the left, like in Ubuntu
    // default: `true` (without backticks and without quotes) on Windows and Linux, ignored on macOS
    showWindowControls: '',

    // custom padding (CSS format, i.e.: `top right bottom left`)
    padding: '12px 14px',

    // the full list. if you're going to provide the full color palette,
    // including the 6 x 6 color cubes and the grayscale map, just provide
    // an array here instead of a color map object
    colors: {
      black: '#000000',
      red: '#C51E14',
      green: '#1DC121',
      yellow: '#C7C329',
      blue: '#0A2FC4',
      magenta: '#C839C5',
      cyan: '#20C5C6',
      white: '#C7C7C7',
      lightBlack: '#686868',
      lightRed: '#FD6F6B',
      lightGreen: '#67F86F',
      lightYellow: '#FFFA72',
      lightBlue: '#6A76FB',
      lightMagenta: '#FD7CFC',
      lightCyan: '#68FDFE',
      lightWhite: '#FFFFFF',
    },

    // the shell to run when spawning a new session (i.e. /usr/local/bin/fish)
    // if left empty, your system's login shell will be used by default
    //
    // Windows
    // - Make sure to use a full path if the binary name doesn't work
    // - Remove `--login` in shellArgs
    //
    // Bash on Windows
    // - Example: `C:\\Windows\\System32\\bash.exe`
    //
    // PowerShell on Windows
    // - Example: `C:\\WINDOWS\\System32\\WindowsPowerShell\\v1.0\\powershell.exe`
    shell: '',

    // for setting shell arguments (i.e. for using interactive shellArgs: `['-i']`)
    // by default `['--login']` will be used
    shellArgs: ['--login'],

    // for environment variables
    env: {},

    // set to `false` for no bell
    bell: 'SOUND',

    // if `true` (without backticks and without quotes), selected text will automatically be copied to the clipboard
    copyOnSelect: false,

    // if `true` (without backticks and without quotes), hyper will be set as the default protocol client for SSH
    defaultSSHApp: true,

    // if `true` (without backticks and without quotes), on right click selected text will be copied or pasted if no
    // selection is present (`true` by default on Windows and disables the context menu feature)
    // quickEdit: true,

    // URL to custom bell
    // bellSoundURL: 'http://example.com/bell.mp3',

    // for advanced config flags please refer to https://hyper.is/#cfg
  },

  // a list of plugins to fetch and install from npm
  // format: [@org/]project[#version]
  // examples:
  //   `hyperpower`
  //   `@company/project`
  //   `project#1.0.1`
  plugins: [
    // theme
    "hyper-dracula",
    
    // productivity
    "hyperline", "hyperlinks", "hyper-tabs-enhanced"
  ],

  backgroundOpacity: '0.1',

  // in development, you can create a directory under
  // `~/.hyper_plugins/local/` and include it here
  // to load it and avoid it being `npm install`ed
  localPlugins: [],

  keymaps: {
    // Example
    // 'window:devtools': 'cmd+alt+o',
  },
};
```

## Étape 5 : Installez la police d'écriture

Installez les polices :
- [MesloLGS NF Regular.ttf](https://github.com/romkatv/dotfiles-public/raw/master/.local/share/fonts/NerdFonts/MesloLGS%20NF%20Regular.ttf)
- [MesloLGS NF Bold.ttf](https://github.com/romkatv/dotfiles-public/raw/master/.local/share/fonts/NerdFonts/MesloLGS%20NF%20Bold.ttf)


## Étape 6 : Les plugins ZSH

Installez [Oh My ZSH](https://github.com/robbyrussell/oh-my-zsh)
```
brew install wget
sh -c "$(wget -O- https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"
```

Modifiez le fichier `~/.zshrc` et ajoutez les plugins qu'on souhaite (on peut ajouter les plugins listés sur [cette page](https://github.com/robbyrussell/oh-my-zsh/tree/master/plugins))
```
vi ~/.zshrc
```

```
plugins=(
  git
  bundler
  dotenv
  osx
  rake
  rbenv
  ruby
)
```

Pour la coloration syntaxique : clonez le repository `zsh-syntax-highlighting` :
```
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```

Puis modifiez le fichier `~/.zshrc` pour activer le plugin en ajoutant cette ligne dans la liste des plugins :
```
plugins=(
  ...
  zsh-syntax-highlighting
)
```

Pour l'auto-complétion : clonez le repository `zsh-autosuggestions` :
```
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```

Puis modifiez le fichier `~/.zshrc` pour activer le plugin en ajoutant cette ligne dans la liste des plugins :
```
plugins=(
  ...
  zsh-autosuggestions
)
```

## Étape 7 : Relancer :)

Fermez Hyper et relancez-le !
