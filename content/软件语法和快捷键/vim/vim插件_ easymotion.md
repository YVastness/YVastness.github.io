
# easymotion
* * *

说明: `<leader>`全局映射为`,`

除却`hjkl`, `gg`, `G`, `Ctrl-D/U`, 以及 `[f/F]<char>`和`[t/T]<char>`这些`vim`默认的移动方式

有没有更高效的移动做法么? 回答是肯定的

这个插件的唯一目的就是: 快速跳转

作用: 如何进行更快速的光标移动

github: [github](https://github.com/Lokaltog/vim-easymotion)

安装
--

```
Bundle 'Lokaltog/vim-easymotion'

```

用法1: 跳转到当前光标前后的位置(w/b)
----------------------

快捷键`<leader><leader>w`(即`,,w`)和`<leader><leader>b`(即`,,b`)

助记: `word` and `back`

演示:

![](https://wklken.me/imgs/vim/easy_motion_base.gif)

easy\_motion\_base.gif

用法2: 搜索跳转(s)
------------

快捷键`<leader><leader>s`(即`,,s`), 然后输入要搜索的字母, 这个跳转是双向的

助记: `search`

演示:

![](https://wklken.me/imgs/vim/easy_motion_search.gif)

用法3: 行级跳转(jk)
-------------

配置

```
map <Leader><Leader>j <Plug>(easymotion-j)
map <Leader><Leader>k <Plug>(easymotion-k)

```

快捷键: `<leader><leader>j`和`<leader><leader>k`(即`,,j`和`,,k`)

助记: `hjkl`不解释

演示:

![](https://wklken.me/imgs/vim/easy_motion_lines.gif)

用法4: 行内跳转(hl)
-------------

配置

```
map <Leader><leader>h <Plug>(easymotion-linebackward)
map <Leader><leader>l <Plug>(easymotion-lineforward)

```

快捷键`<leader><leader>h`和`<leader><leader>l`(即`,,h`和`,,l`)

助记: `hjkl`不解释

![](https://wklken.me/imgs/vim/easy_motion_inline.gif)

用法5: 重复上一次动作(.)
---------------

配置

```
map <Leader><leader>. <Plug>(easymotion-repeat)

```

快捷键`<leader><leader>.`

助记: 同`repeat`插件….

![](https://wklken.me/imgs/vim/easy_motion_repeat.gif)

* * *

最终配置
----

```
Bundle 'Lokaltog/vim-easymotion'
let g:EasyMotion_smartcase = 1
"let g:EasyMotion_startofline = 0 " keep cursor colum when JK motion
map <Leader><leader>h <Plug>(easymotion-linebackward)
map <Leader><Leader>j <Plug>(easymotion-j)
map <Leader><Leader>k <Plug>(easymotion-k)
map <Leader><leader>l <Plug>(easymotion-lineforward)
" 重复上一次操作, 类似repeat插件, 很强大
map <Leader><leader>. <Plug>(easymotion-repeat)

```

* * *

建议
--

1.  还可以`<Leader><leader>f`和`<Leader><leader>t`, 不过建议简单化, 一个`<Leader><leader>w/b`走天下.
    
2.  如果你不经常使用`s`, 可以将`s`改键, `nmap s <Plug>(easymotion-s)`, 这样你只需要输入`s`就可以进行搜索快速跳转(强迫症表示不能忍….) 具体做法见[官方文档](https://github.com/Lokaltog/vim-easymotion#bidirectional-motions)
    
3.  默认`<leader><leader>`作为这个插件的快捷键其实挺好的, 貌似没有其他插件会导致冲突, 还可以配置一整套, 强迫症很满意
    
4.  可以配置2/n个字符的搜索跳转, 更精准, 按需自取(个人觉得太复杂了没必要) [文档](https://github.com/Lokaltog/vim-easymotion#2-character-search-motion)和[文档](https://github.com/Lokaltog/vim-easymotion#n-character-search-motion)
    
5.  这个插件专心做好跳转就好, 没必要把搜索的活给做了