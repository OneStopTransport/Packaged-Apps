Leaflet App
============

Aplicação que permite desenhar círculos no mapa, usando a biblioteca [Leaflet](http://leafletjs.com), e obter paragens e percursos de autocarro que intersectam os círculos desenhados.

## Estrutura

A aplicação é constituída pelos seguintes ficheiros:

* `config.xml` - Ficheiro de configuração, necessário a cada *packaged app*, que identifica a aplicação, o autor e descreve o propósito da mesma;
* `icon.png` - Logótipo da aplicação que aparecerá no *marketplace*, depois de submetida a aplicação;
* `images` - Pasta com as imagens para os botões que controlam o mapa, entre outros; 
* `index.html` - Página HTML com o mapa e a invocação à API de obtenção de paragens e percursos de autocarros;
* `leaflet.js` - Biblioteca *Javascript* para desenho e interacção com mapas;
* `leaflet.css` - Folha de estilos para o aspecto dos botões, etiquetas, figuras e mapa;
* `README.md` - Texto de introdução à aplicação.



## Requisitos

Para o correcto funcionamento da aplicação é necessário o seguintes elemento:

* **Chave de API OST para Browser**: https://developer.ost.pt/docs/guia_do_programador/conceitos_chave/


## Instruções

1. Alterar o ficheiro `config.xml`, em particular o campo `id` do elemento `widget` e os elementos `name` e `description`:

	```xml
	<widget xmlns="http://www.w3.org/ns/widgets" id="http://widgets.tice.ipn.pt/YOUR_ID_HERE" fullscreen="true" version="1.0.0">
      <name short="YOUR APP NAME HERE">YOUR APP SMALL DESCRIPTION HERE</name>
      <description>YOUR APP DESCRIPTION HERE</description>
      <content src="index.html" />
      <icon src="icon.png" />
   	  <author>YOUR NAME HERE</author>
	</widget>
	```
	
2. Alterar o ficheiro `index.html` nomeadamente nas seguintes linhas:
	
	**Linha 16**: No caso de se querer testar localmente esta app (abrindo o ficheiro no *browser*), não deverá funcionar pois os protocolos de invocação das API e das bibliotecas não será o `file://` mas sim o `https://`, portanto tem de se substituir as duas barras por `https://`.
	
	**Linha 109**: Trocar `YOUR_OST_KEY` pela chave de API da OST pedida nos Requisitos
	
	```javascript
	 var params = {
	 	key:    'YOUR_OST_KEY',
        center: center.lng+','+center.lat,
	```

3. Para poderem submeter a vossa aplicação alterada na plataforma OST, basta seguirem os passos presentes na secção **Instruções** e **Submissão na OST** do [README](../README.md) do projecto.


---

## Ajuda

Podem usar o [**Fórum de Suporte**](https://support.ost.pt/everyone/) para deixarem as vossas dúvidas e sugestões.










