This repo contains a collection of NERD snippets. (http://github.com/scrooloose/nerdsnippets).

It contains:
* my personal snippets
* many of the snippets from scrooloose. (http://github.com/scrooloose/snippets)
* some of the rails related snippets converted from textmate by Fabio Akita (http://github.com/akitaonrails)

To use these snippets, you have to tell NERD snippets about them. The easiest way to do this is to create a snippet setup file here: 
    ~/.vim/after/plugin/snippet_setup.vim

Call the file whatever you want, but its important to stick it in the after/plugin directory.  This setup file could look something like the following:


call NERDSnippetsReset()
source ~/.vim/snippets/support_functions.vim
call NERDSnippetsFromDirectory("~/.vim/snippets")

"use our html snippets for eruby and xhtml too
call NERDSnippetsFromDirectoryForFiletype('~/.vim/snippets/ruby-rails', 'ruby')
call NERDSnippetsFromDirectoryForFiletype('~/.vim/snippets/eruby-rails', 'eruby')
call NERDSnippetsFromDirectoryForFiletype('~/.vim/snippets/html', 'eruby')


