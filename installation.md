---
layout: default
title: 4. Instalação - Como Instalar o openSUSE No Seu Computador
permalink: instalacao
---

# 4. Instalação

Esta é apenas uma breve descrição da instalação do openSUSE. Para uma ajuda mais minuciosa, veja a documentação oficial.

## 4.1 Antes de instalar

Antes de começar, você deve se atentar a algumas coisas.

### 4.1.1 Requisitos mínimos do sistema

- **CPU:** processador AMD64 ou Intel64
- **Memória RAM:** pelo menos 1GB (o recomendado são 2GB)
- **Espaço em disco:** pelo menos 5GB para uma instalação comum (o recomendado é ter mais espaço)
- **Placas de vídeo e de som:** a maioria das placas atuais são suportadas

### 4.1.2a Gravando a imagem ISO em um DVD

Ao gravar a imagem ISO baixada em um DVD, é importante lembrar de escolher a opção ISOs ou imagens em seu programa gravador de DVD, ou a mídia não será bootável.

### 4.1.2b Criando um pendrive bootável

A imagem ISO também pode ser gravada em um *pendrive*, veja as instruções de como fazer isso nessas páginas, dependendo de quais sistemas operacionais você dispõe no momento:

- openSUSE ou outro Linux: [http://en.opensuse.org/SDB:Live_USB_stick](http://en.opensuse.org/SDB:Live_USB_stick)
- Microsoft Windows: [https://en.opensuse.org/SDB:Create_a_Live_USB_stick_using_Windows](https://en.opensuse.org/SDB:Create_a_Live_USB_stick_using_Windows)
- Mac OS X: [https://en.opensuse.org/SDB:Create_a_Live_USB_stick_using_Mac_OS_x](https://en.opensuse.org/SDB:Create_a_Live_USB_stick_using_Mac_OS_x)

### 4.1.3 Configurar a BIOS

Se seu computador não bootar pelo DVD ou *pendrive*, verifique se a BIOS do computador está configurada para bootar pelo DVD ou *pendrive*.

### 4.1.4 Dual boot (openSUSE e Windows no mesmo computador)

Ter openSUSE e Windows instalados no mesmo computador normalmente é muito simples se o Windows foi instalado primeiro. Durante a instalação, o openSUSE detectará o Windows. Depois, cada vez que você ligar o computador, o gerenciador de *boot* (*bootloader*) apresentará um menu permitindo escolher qual sistema iniciar: openSUSE ou Windows.

O openSUSE precisa ser instalado em uma partição separada ou em um disco separado. É recomendado liberar espaço em disco antes de usar a ferramenta de particionamento que você está familiarizado. Mas você também pode deixar o instalador do openSUSE redimensionar as partições do Windows — nesse caso, é fortemente recomendado desfragmentar a partição do Windows antes de começar a instalação.

### 4.1.5 Conecte o cabo de rede e ligue os periféricos

Se você conectar seu cabo de rede e ligar sua impressora e outros periféricos antes de começar a instalação, há uma boa chance de que eles sejam autodetectados e configurados.

## 4.2 O processo de instalação

Quando estiver pronto, insira o DVD ou *pendrive* e reinicie (ou ligue) o computador.

### Início

<table>
	<tr>
		{% include installation.html image="grub" %}
		<td valign="top">Você será apresentado ao menu do gerenciador de <em>boot</em> do DVD ou <em>pendrive</em>.<br /><br />

		Aqui você pode selecionar seu idioma desejado e mais algumas opções, depois comece a instalação.</td>
	</tr>
</table>

### Idioma, teclado e contrato de licença

<table>
	<tr>
		{% include installation.html image="inst-welcome" %}
		<td valign="top">O contrato de licença é apenas para te informar dos seus direitos. Ele não requer sua aceitação, uma vez que ele não limita seu uso.<br /><br />

		Verifique se as configurações de idioma e teclado estão como desejado.</td>
	</tr>
</table>

### Particionamento

<table>
	<tr>
		{% include installation.html image="inst-disk" %}
	  <td valign="top">Por padrão, o openSUSE vai sugerir a criação de três novas partições: (1) <code>/</code> (raiz), para os arquivos do sistema; (2) <code>/home</code> para os arquivos pessoais do(s) usuário(s); e (3) <code>swap</code> que é um espaço do disco rígido utilizado em complemento à memória RAM, semelhante ao arquivo de paginação do Windows.<br /><br />

	  Não se preocupe com os subvolumes criados, são apenas detalhes técnicos do sistema de arquivos Btrfs, e não partições "reais", com que usuários normais deveriam se preocupar.<br /><br />

	  Sempre verifique se o particionamento sugerido é o que você quer, e se você está fazendo uma instalação <em>dual boot</em>, redobre a atenção, para se certificar de que tudo está conforme o desejado.<br /><br />

	  Note que o Linux identifica os discos e partições da seguinte forma: <i>sda1</i> é a primeira partição do primeiro disco, <i>sdb3</i> é a terceira partição do segundo disco, e assim por diante. Partições que serão formatadas são destacadas em vermelho.</td>
	</tr>
</table>

### Relógio e fuso horário

<table>
	<tr>
		{% include installation.html image="inst-time" %}
		<td valign="top">Defina o fuso horário aqui.<br /><br />

Se você usa apenas GNU/Linux é recomendado definir o relógio do <em>hardware</em> como UTC. Se você faz <em>dual boot</em> com Windows, desmarque essa opção (relógio do <em>hardware</em> armazenará hora local).</td>
	</tr>
</table>

### Interface de usuário

<table>
	<tr>
		{% include installation.html image="inst-desktop" %}
		<td valign="top">Várias diferentes interfaces gráficas (ambientes de trabalho) existem para o GNU/Linux. A área de trabalho com KDE Plasma é pré-selecionada, é a preferida por cerca de 70% dos usuários do openSUSE e é também o foco deste guia. Mas você também pode escolher a área de trabalho com GNOME ou uma instalação de servidor, com interface textual.<br /><br />

		Em "Personalizado" você pode selecionar manualmente diferentes padrões, incluindo áreas de trabalho leves como Xfce e LXDE.</td>
	</tr>
</table>

### Criar Novo Usuário

<table>
	<tr>
	{% include installation.html image="inst-user" %}
	<td valign="top">Agora é hora de criar sua conta de usuário. Note que por padrão a senha do usuário <em>root</em> (administrator) será igual à do usuário normal.<br /><br />

	Se você quer a segurança adicional de uma senha de administrador diferente, considere desmarcar essa opção. Você também pode querer desabilitar o <em>login</em> automático para prevenir que pessoas acessem facilmente seu sistema e dados.</td>
	</tr>
</table>

### Configurações da instalação

<table>
	<tr>
		{% include installation.html image="inst-overview" %}
		<td valign="top">Se certifique de que tudo está conforme o desejado — uma vez passada essa tela, não haverá volta!</td>
	</tr>
</table>

### Instalação propriamente dita

<table>
	<tr>
		{% include installation.html image="inst-inst" %}
		<td valign="top">Agora é feita a instalação propriamente dita: o sistema operacional é copiado para o disco e configurado. Quando terminar, o computador será reiniciado e o sistema estará pronto para uso.<br /><br />

Divirta-se bastante com o openSUSE!
		</td>
	</tr>
</table>
