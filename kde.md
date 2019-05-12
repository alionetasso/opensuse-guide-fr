---
layout: default
title: 5. Ambiente de trabalho KDE Plasma - Use e Configure o KDE no Desktop ou Netbook
permalink: kde
---

# 5. Ambiente de trabalho KDE Plasma

O ambiente de trabalho KDE Plasma é uma das primeiras coisas que você verá quando você iniciar o openSUSE Leap pela primeira vez. O ambiente de trabalho consiste da área de trabalho, menus, painéis, gerenciamento de arquivos e gerenciamento de janelas.

O ambiente de trabalho KDE Plasma é bastante configurável. Se há alguma coisa que não te agrada, é quase certo que você pode configurá-la de acordo com suas preferências. É também bastante rico em funcionalidades. Abaixo são mencionadas apenas as funcionalidades mais básicas.

## 5.1 A área de trabalho

A área de trabalho não é muito diferente de outras áreas de trabalho que provavelmente você está familiarizado — você tem um painel embaixo e um menu de lançamento é aberto ao clicar no botão no canto inferior esquerdo.

No entanto, algumas coisas diferem significativamente da maioria das outras áreas de trabalho:

- o KDE usa o *clique único* para abrir arquivos e iniciar programas por padrão; e
- por padrão, quando você desliga o computador, os aplicativos que você está usando serão iniciados novamente quando você ligar o computador.

{% include screenshot.html image="desktop" %}

### 5.1.1 O lançador de aplicativos

O lançador de aplicativos é aberto clicando no ícone no canto inferior esquerdo da tela ou pressionando a tecla **Super** ou **Alt + F1**. Abaixo no menu há uma caixa de pesquisa e no topo esquerdo estão seus aplicativos favoritos. Você pode adicionar ou remover aplicativos dos favoritos clicando o botão direito do *mouse* neles.

{% include screenshot.html image="launchmenu" %}

Você pode editar itens do menu ou adicionar novos itens assim:

<div class="path">Clique com o botão direito do <em>mouse</em> no ícone do lançador =&gt; Clique em "Editar aplicativos"</div>

Para adicionar um atalho para um aplicativo na área de trabalho ou no painel você pode fazer assim (requer que os *widgets* estejam desbloqueados):

<div class="path">Localize o aplicativo no lançador => Clique com o botão direito do <em>mouse</em> => Clique em "Adicionar à área de trabalho" ou "Adicionar ao painel"</div>

### 5.1.2 Áreas de trabalho virtuais

Para evitar que sua área de trabalho fique bagunçada com várias janelas, você pode usar áreas de trabalho virtuais para organizar seus aplicativos e ser mais produtivo. No painel você encontra uma pequena grade, esse é o paginador de áreas de trabalho, use-o para alternar entre suas áreas de trabalho virtuais.

<center><img src="{{ site.baseurl | append: '/images/screenshots/pager.png' | replace: '//', '/' }}" alt="pager" class="pic" /></center>

Você também pode usar o efeito grade da área de trabalho para ter uma visão geral em tela cheia das suas áreas de trabalho virtuais, experimente pressionar **Ctrl + F8** (requer suporte a efeitos da área de trabalho, leia mais sobre isso adiante).

## 5.2 Gerenciamento de arquivos

O gerenciador de arquivos padrão é o Dolphin. Você pode encontrá-lo como um dos favoritos no lançador de aplicativos ou na categoria "Sistema". Usá-lo deve ser intuitivo. <em>Pendrives</em> e outras mídias removíveis aparecerão automaticamente no painel esquerdo do Dolphin.

<div class="path">Lançador de aplicativos => Aplicativos => Sistema => Gerenciador de arquivos (Dolphin)</div>

Você também pode encontrar o Dolphin como um dos favoritos no lançador de aplicativos.

{% include screenshot.html image="dolphin" %}

## 5.3 Configurações da área de trabalho

As configurações globais do KDE estão convenientemente reunidas em um único lugar. Aqui você pode configurar praticamente qualquer coisa relacionada ao ambiente de trabalho KDE Plasma, incluindo comportamento do *mouse*, aplicativos padrão, associações de arquivos, etc.

<div class="path">Lançador de aplicativos => Aplicativos => Configurações => Configurações do sistema</div>

Você também pode encontrar o aplicativo Configurações do sistema como um dos favoritos no lançador de aplicativos.

{% include screenshot.html image="systemsettings" %}<p></p>

{% include tip.html tip="Não confunda o aplicativo Configurações do sistema do KDE, usado para configurações pessoais do ambiente de trabalho KDE e dos aplicativos do KDE, com o Centro de controle do YaST, usado para configurações de administrador em um nível mais profundo do sistema (ver capítulo sobre o YaST mais adiante)." %}

## 5.4 Monitor do sistema / Tabela de processos

Naturalmente o KDE também tem uma ferramenta para monitorar processos em execução e utilização de recursos do sistema. Simplesmente pressione **Ctrl + Esc** para mostrar a janela Atividade do sistema.

{% include screenshot.html image="systemactivity" %}

Para um monitor de sistema avançado e personalizável, incluindo gráficos de rede, entre outros recursos, use o programa KSysGuard.

## 5.5 Widgets

A área de trabalho KDE Plasma é centrada em *widgets* e contêineres. A área de trabalho e o painel são contêineres nos quais *widgets* podem ser adicionados. O lançador de aplicativos, a área de notificação, etc. são simplesmente *widgets*. Muitos outros *widgets* estão disponíveis.

Para adicionar widgets:

<div class="path">Clique com o botão direito do <em>mouse</em> na área de trabalho => Adicionar widgets => Arraste <em>widgets</em> para a área de trabalho ou para um painel</div>

Para configurar, mover, redimensionar *widgets*, etc. clique no canto superior direito da área de trabalho para abrir a caixa de ferramentas. Isso requer que os *widgets* estejam desbloqueados.

<div class="path">Clique com o botão direito do <em>mouse</em> na área de trabalho => Clique em "Bloquear widgets" ou "Desbloquear widgets".</div><br/>

{% include screenshot.html image="widgets" %}

## 5.6 Efeitos da área de trabalho

O gerenciador de janelas do KDE tem suporte embutido para efeitos 3D da área de trabalho. Uma seleção básica e discreta de efeitos será habilitada por padrão se você tiver o *hardware* apropriado e os devidos *drivers* instalados. Experimente pressionar **Ctrl + F8** ou **Ctrl + F9**, por exemplo.

Você pode desabilitar ou habilitar outros/mais efeitos nas Configurações do sistema.

{% include screenshot.html image="effects" %}

O atalho de teclado para temporariamente habilitar ou desabilitar os efeitos da área de trabalho é **Alt + Shift + F12**.
