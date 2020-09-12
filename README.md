# Configuração do Openbox
 Essa é a minha config pessoal do Openbox WM, mas que está disponível para aqueles que quiserem uma config pronta do Openbox.
 
 ![Alt text](demonstration.png?raw=true "Optional Title")

O tema usado é o Dracula Theme, que pode ser acessado pelo [site oficial](https://draculatheme.com/), mas para ajudar, eu reuni nesse repositório: o tema Dracula para o Telegram Desktop; o tema GTK do Dracula; e o Dracula para Openbox, que é um tema de gerenciador de janelas (wm)


## Programas para instalar:
-------------
### dmenu
Instale o DMENU, para usar como menu ao invés de do próprio do openbox

Dê esse comando para atualizar:

$ sudo pacman -Syu

E esse para instalar o dmenu:

$ sudo pacman -S dmenu

-------------
### nitrogen

Nitrogen é um programa simples e leve para os seus wallpapers
Sua instalação é tão simples quanto a do dmenu:

$ sudo pacman -S nitrogen

-------------
### polybar

A instalação da polybar é compilação, para ser mais simples vamos usar o 'yay'. Se você não tiver ele, aqui está um [vídeo ensinando como instalar o yay](https://www.youtube.com/watch?v=BbnSoY_yDr8)

A polybar pode ser instalada por qualquer AUR Helper, como o pamac, mas aqui mostrarei com o yay:

$ yay -S polybar

Agora, precisamos instalar a Powerline, um ótimo pacote de fontes para a polybar. Para isso execute:

$ sudo pacman -S git
$ git clone https://github.com/powerline/fonts.git
$ cd fonts
$ ./install.sh

Agora vamos instalar outro pacote de fontes, a Siji, que vai fornecer os ícones para a barra

$ yay -S siji-git

Polybar instalado, fontes instaladas, agora só falta configurar. Primeiro, vamos adicionar as configurações deste repositório que está dentro do diretório polybar.

Faça o download do .zip, ou clone esse repositório com:

$ git clone https://github.com/dakidev/openbox.git

Depois, crie a pasta de configurações:

$ mkdir -p ~/.config/polybar

Agora, vamos instalar uma barra de exemplo da polybar:

$ install -Dm644 /usr/share/doc/polybar/config $HOME/.config/polybar/config

Teste essa barra com o seguinte comando, e após admirar ela, pressione Control+C para continuarmos:

$ polybar -r example

Agora, vamos alterar a configuração de exemplo para a configuração desse repositório. Para isso, você pode substituir a pasta dentro de 
/home/(seu usuário)/.config/
pelo diretório polybar desse repositório.

Para executar a barra, basta dar o comando:

$ polybar -r mybar

Na configuração do openbox presente nesse repositório, a polybar e o nitrogen já foram adicionados para a autoinicialização. Esse tutorial de instalação da polybar foi baseada [nesse tutorial](https://sup3r-us3r.github.io/10/08/2018/como-instalar-e-configurar-o-polybar#:~:text=INSTALA%C3%87%C3%83O,polybar%20atrav%C3%A9s%20do%20reposit%C3%B3rio%20oficial.)

-------------
