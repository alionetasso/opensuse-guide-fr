---
layout: default
title: 2. Migrando para o GNU/Linux - Vantagens e Desafios de Migrar para o GNU/Linux
permalink: migrando
---

# 2. Migrando para o GNU/Linux

Migrar para um sistema operacional novo e muito diferente requer um grande esforço, ainda que seja no mesmo computador — claro que você não precisa migrar completamente, nada te impede de usar dois ou mais sistemas operacionais. Este capítulo descreve alguns pontos que você deve considerar antes de se aventurar no maravilhoso mundo do GNU/Linux.

## 2.1 Por que usar GNU/Linux?

Há muitos motivos pelos quais milhões de pessoas gostam de usar o GNU/Linux — motivos de natureza técnica, financeira, ética ou filosófica, dependendo do ponto de vista de cada pessoa. Aqui está uma lista de alguns dos motivos mais comuns para escolher o GNU/Linux:

- **Segurança:** praticamente não existem vírus para Linux, assim como *spyware* ou outras ameaças;
- **Manutenção:** esqueça a preocupação com escanear arquivos em busca de vírus, desfragmentar o disco, limpar o registro, reiniciar o computador, etc.;
- **Estabilidade:** o GNU/Linux é muito estável. Aplicativos podem travar individualmente, mas o próprio sistema operacional travar é muito raro;
- **_Software_ livre/código aberto:** você pode usar o *software* como quiser, estudar o código-fonte, modificá-lo, compartilhá-lo. Nenhum contrato de licença com letras miúdas;
- **Padrões abertos:** o GNU/Linux e os aplicativos desenvolvidos para ele geralmente suportam padrões abertos, possibilitando perfeita interoperação com outras plataformas e evitando a dependência de fornecedores (*vendor lock-in* — [aprisionamento tecnológico](https://pt.wikipedia.org/wiki/Aprisionamento_tecnol%C3%B3gico));
- **Comunidade:** o GNU/Linux tem sido descrito como um "esporte de um time só internacional";
- **Economia:** a maior parte das distribuições GNU/Linux podem ser baixadas de graça e o mesmo se aplica para uma imensa quantidade de aplicativos disponíveis para elas. Além disso, requisitos de *hardware* comparativamente modestos significam que você não terá que comprar novo *hardware* com frequência;
- **Legalidade:** acesso a *software* de alta qualidade, de graça e legalmente significa menor tentação a usar cópias ilegais não autorizadas de *softwares* proprietários. Você também não estará apoiando um monopolista conhecido por várias condenações por abusar de sua posição dominante no mercado;
- **Transparência:** a maior parte das distribuições GNU/Linux são desenvolvidas em espaços abertos, usando listas de *e-mail* públicas, canais de IRC públicos, rastreadores de *bugs* (*bug trackers*) públicos, rastreadores de recursos (*feature trackers*) públicos, etc.;
- **Diversidade:** existem várias distribuições GNU/Linux desenvolvidas por diferentes empresas ou projetos comunitários, para diferentes propósitos, fornecendo diferentes experiências de usuário;
- **Privacidade:** *softwares* livres geralmente respeitam sua privacidade, e código-fonte disponibilizado publicamente oferece alguma proteção contra *backdoors* e semelhantes;
- **Experimentar algo novo**: o simples fato de experimentar algo novo e diferente pode ser, por si só, uma motivação para muitas pessoas; e...
- **é muito divertido!**

{% include pic.html image="hardware.gif" %}

## 2.2 Desafios de migrar

Apesar das várias vantagens de usar o GNU/Linux, também pode ser desafiador mudar para algo novo, diferente e menos *mainstream* (menos comum):

- **Curva de aprendizado:** você precisará aprender como usar um sistema operacional novo e um tanto diferente, assim como novos aplicativos — e você terá que *desaprender* muito do que aprendeu usando outros sistemas operacionais;
- **Falta de aplicativos e jogos:** você pode sentir falta de aplicativos que lhe são familiares, comumente o Microsoft Office, o Adobe Photoshop e a maior parte dos jogos grandes e populares. *Dual boot*, WINE e máquinas virtuais oferecem soluções parciais para esse problema. E, claro, existem alternativas de alta qualidade próprias para GNU/Linux;
- **Falta de suporte a determinado _hardware_:** a maioria dos dispositivos são suportados, mas não todos — antes de comprar novos componentes de _hardware_, pesquise na Internet se alguém já os utiliza com GNU/Linux. Componentes mais novos e menos difundidos têm mais chances de apresentar problemas no funcionamento; e
- **Maior dificuldade em obter ajuda:** muitas vezes amigos, familiares e colegas de trabalho não conseguirão te ajudar se você tiver problemas com o GNU/Linux, por isso pode ser que você precise pedir ajuda *online*, o que com frequência não é tão efetivo quanto obter ajuda ao vivo com alguém conhecido.

## 2.3 Estratégia

Uma vez que a migração nem sempre é fácil, aqui vai alguns conselhos:

- **Seja realista:** não espere dominar o GNU/Linux em uma semana ou duas, como você dominou o sistema operacional anterior depois de, talvez, 10 anos usando-o ou mais. E não espere que o GNU/Linux seja perfeito;
- **Mude gradualmente:** comece instalando o GNU/Linux em um segundo computador, ou em *dual boot* com seu sistema operacional anterior, ou quem sabe em uma máquina virtual. Comece aprendendo o básico e resolva problemas com calma, um de cada vez; e
- **Peça ajuda:** não se acanhe de pedir ajuda na Internet, no trabalho, a um amigo ou em qualquer outro lugar.

### 2.3.1 Aplicativos para GNU/Linux disponíveis também para Windows e Mac OS X

Se você começar a usar aplicativos para GNU/Linux no sistema operacional que você já usa, migrar depois será muito mais fácil. Estes são alguns exemplos de aplicativos gratuitos para as tarefas mais comuns disponíveis tanto para GNU/Linux quanto para Windows (muitos deles estão disponíveis para Mac OS X também):

<table width="98%">
	<tbody><tr>
		<td class="small-bold"><em>Softwares</em> livres</td>
		<td class="small-bold"></td>
		<td class="small-bold"><em>Softwares</em> proprietários</td>
	</tr>

	<tr>
		<td valign="top">
		<a href="http://www.mozilla.org/firefox/" target="_blank">Firefox</a> (navegador)<br>
		<a href="http://www.mozilla.org/thunderbird/" target="_blank">Thunderbird</a> (cliente de <em>e-mail</em>)<br>
		<a href="http://www.seamonkey-project.org/" target="_blank">SeaMonkey</a> (suíte de Internet)<br>
		<a href="http://www.pidgin.im/" target="_blank">Pidgin</a> (mensagens instantâneas)<br>
		<a href="http://filezilla-project.org/" target="_blank">FileZilla</a> (cliente FTP)<br>
		<a href="http://qbittorrent.sourceforge.net/" target="_blank">qBittorent</a> (cliente BitTorrent)<br>
		<a href="http://www.qutecom.org/" target="_blank">QuteCom</a> (VoIP)<br>
		<a href="http://www.linphone.org/" target="_blank">Linphone</a> (VoIP)<br>
		<a href="http://gpodder.org/" target="_blank">gPodder</a> (gerenciador de <em>podcasts</em>)<br>
		<a href="http://bluegriffon.org/" target="_blank">BlueGriffon</a> (editor de HTML)<br>
		<a href="http://gimp-win.sourceforge.net/" target="_blank">GIMP</a> (editor de imagens avançado)<br>
		<a href="http://www.inkscape.org" target="_blank">Inkscape</a> (desenho vetorial)<br>
		<a href="http://hugin.sourceforge.net/" target="_blank">Hugin</a> (geração de panoramas)<br>
		<a href="http://www.libreoffice.org/" target="_blank">LibreOffice</a> (suíte de escritório)<br>
		<a href="http://www.scribus.net/" target="_blank">Scribus</a> (programa de paginação)<br>
		<a href="http://gnucash.org/" target="_blank">GnuCash</a> (gestão de finanças)<br>
		</td>
	<td valign="top">
    <a href="http://www.abisource.com/" target="_blank">Abiword</a> (processador de textos simples)<br />
    <a href="http://sourceforge.net/projects/free-cad/" target="_blank">FreeCAD</a> (CAD 3D)<br />
    <a href="http://librecad.org/" target="_blank">LibreCAD</a> (CAD 2D)<br />
    <a href="http://www.blender.org" target="_blank">Blender</a> (animação 3D)<br />
    <a href="http://calibre-ebook.com/" target="_blank">Calibre</a> (gerenciador de <em>e-books</em>)<br />
    <a href="http://www.videolan.org/" target="_blank">VLC</a> (reprodutor multimídia)<br />
    <a href="http://smplayer.sourceforge.net/" target="_blank">SMPlayer</a> (reprodutor multimídia)<br />
    <a href="http://www.clementine-player.org/" target="_blank">Clementine</a> (reprodutor de música)<br />
    <a href="http://audacity.sourceforge.net/" target="_blank">Audacity</a> (edição de áudio)<br />
    <a href="http://lmms.sourceforge.net/" target="_blank">LMMS</a> (produção musical)<br />
    <a href="http://kid3.sourceforge.net" target="_blank">Kid3</a> (editor de <em>tags</em> de áudio)<br />
    <a href="http://edu.kde.org/marble/download.php" target="_blank">Marble</a> (globo virtual)<br />
    <a href="http://gramps-project.org/" target="_blank">Gramps</a> (árvore genealógica)<br />
    <a href="https://edu.kde.org/kstars/#download" target="_blank">KStars</a> (astronomia)<br />
    <a href="http://www.stellarium.org/" target="_blank">Stellarium</a> (astronomia)<br />
	</td>
	<td valign="top">
		<a href="http://opera.com/" target="_blank">Opera</a> (navegador)<br>
		<a href="https://www.google.com/chrome" target="_blank">Google Chrome</a> (navegador)<br>
		<a href="http://www.skype.com" target="_blank">Skype</a> (VoIP)<br>
		<a href="http://earth.google.com/" target="_blank">Google Earth</a> (globo virtual)<br>
		<a href="http://www.adobe.com" target="_blank">Adobe Reader</a> (leitor de PDF)<br>
		<a href="http://www.desura.com/" target="_blank">Desura</a> (serviço de distribuição de jogos)<br>
		<a href="http://www.3ds.com/products/draftsight/free-cad-software/" target="_blank">Draftsight</a> (CAD)<br>
	</td>
	</tr>
</tbody></table>

Muitos dos aplicativos do KDE (ver próximos capítulos) também estão disponíveis para Windows e Mac OS X. No entanto, eles estão em um estágio inicial nesses sistemas operacionais. Para mais informações, consulte:

- [http://windows.kde.org](http://windows.kde.org)
- [http://mac.kde.org](http://mac.kde.org)

No Mac OS X, você pode instalar aplicativos do KDE e vários outros *softwares* livres por meio do [Projeto MacPorts](http://www.macports.org/) ou do [Projeto Fink](http://www.finkproject.org/).
