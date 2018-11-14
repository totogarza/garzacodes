---
layout: post
title: Neovim para principiantes configuraciones
date: 2018-11-11 18:01 -0700
tags: neovim
---

En el video anterior vimos cuestiones muy básicas sobre neovim y como te habrás percatado el editor se veía muy austero y poco amigable así que en esta ocasión solucionaremos eso configurando nuestro entorno.

Una vez que veas como se hace tú podrás buscar la manera de configurar neovim a tu gusto.

Cuando inicia vim este primero hace echa un vistazo en el sistema en búsqueda del archivo de configuración, en el caso de neovim este archivo se llama __init.vim__ (.vimrc en el caso de vim).

Si este archivo no existe o está en blanco nvim continuará con una configuración predeterminada la cual  es muy básica y es por esta razón que buscamos realizar ajustes para agregarle funcionalidades que queremos tener.

Para extender las funcionalidades de vim podemos recurrir a plugins y para instalar estos existen múltiples maneras y la más fácil es usando algún manejador de paquetes.

Existen varios manejadores de paquetes:

- Vundle
- NeoBundle
- VimPlug
- Pathogen

En mi caso yo uso __NeoBundle__ pero eres libre que elgir el manejador que prefieras.

Ahora debemos buscar algún plugin de nuestro interés y estoy pensando el algunos que podrían ser de tu interés.

- NERDTree
- Airline
- EasyMotion


Antes de ir a instalar plugins también debes saber que el archivo de configuración (init.vim) no solo sirve para mantener el registro de tus plugins si no que también es el lugar donde podrás mapear teclas para realizar ciertos acciones o hacer por ejemplo ejecutar comandos ya existentes en vim a iniciar el editor (por ejemplo mostrar el número de línea a la izquierda del editor)

```{vim}

```

## Referencias


https://www.youtube.com/watch?v=8UsIexAY4NY

https://www.npmjs.com/package/tern

https://medium.com/@alexlafroscia/writing-js-in-vim-4c971a95fd49

https://hackernoon.com/5-vim-plugins-i-cant-live-without-for-javascript-development-f7e98f98e8d5

https://www.gregjs.com/vim/2016/neovim-deoplete-jspc-ultisnips-and-tern-a-config-for-kickass-autocompletion/

https://vimawesome.com/plugin/deoplete-nvim

https://fortes.com/2017/language-server-neovim/

http://ternjs.net/doc/manual.html

https://www.reddit.com/r/neovim/comments/63e3h4/javascript_autocompletion_with_deoplete/

https://github.com/sourcegraph/javascript-typescript-langserver

https://github.com/autozimu/LanguageClient-neovim

https://codekoalas.com/blog/setting-neovim-javascript-development

https://hackernoon.com/using-neovim-for-javascript-development-4f07c289d862
