# Vim Unity Snippets

A collection of snippets for Unity development.

## Snippet Engines suporting vim-unity-snippets

Snippets are supported by the following engines:
* [SirVer/ultisnips](https://github.com/SirVer/ultisnips): python, supports all snippets in this repo.
* [garbas/vim-snipmate](garbas/vim-snipmate): VimL, snipmate-snippets, engine sometimes behaves strange. Supports snippets/*
* [Shougo/neosnippet](https://github.com/Shougo/neosnippet.vim): VimL, supports snippets/* with some configuration.

Note: I only use UltiSnips so I did not test these snippets on the other engines. If someone does, please tell me your experience. So I can update this readme for other readers.

## Installation

### UltiSnips & Vim-Plug

Add the following lines to your .vimrc:
```
Plug 'Mathijs-Bakker/vim-unity-snippets'
```
(Don't forget to do ``:PlugInstall``)

And add ``"UnitySnippets"`` to UltiSnipsSnippetDirectories.

```
let g:UltiSnipsSnippetDirectories=["UnitySnippets"]
```

**Example .vimrc:**
```
call plug#begin('~/.vim/plugged')
  Plug 'SirVer/ultisnips'
  Plug 'honza/vim-snippets'
  Plug 'Mathijs-Bakker/vim-unity-snippets'
call plug#end()

let g:UltiSnipsSnippetDirectories=["UltiSnips", "UnitySnippets"]
```

When you experience any issues read [:h ultisnips](https://github.com/SirVer/ultisnips/blob/master/doc/UltiSnips.txt).

#### Extenject / Zenject snippets activation:
Add ``"ZenjectSnippets"`` to UltiSnippetDirectories.

```
let g:UltiSnipsSnippetDirectories=["UltiSnips", "UnitySnippets", "ZenjectSnippets"]
```

## Snippets
### UnitySnippets
| Tab trigger    | Description/output                            |
|----------------|-----------------------------------------------|
| assetmenu      | CreateAssetMenu attribute                     |
| cor            | Coroutine (method)                            |
| cotimer        | Coroutine timer (method)                      |
| dl             | ``Debug.Log();``                              |
| sf             | ``[SerializedField]``                         |
| sfield         | ``[SerializedField] private $type $name``     |
| utest          | Playmode test (method)                        |
| sprop          | Unity property with serialized backing field  |

### ZenjectSnippets
| Tab trigger    | Description/output                            |
|----------------|-----------------------------------------------|
| zctor          | MonoBehaviour constructor                     |
| ztest          | Zenject unit test fixture file template (TDD) |  
