# jQuery GeoRegionalizacion - Chile

![jQuery GeoRegionalizacion - Chile](https://i.imgur.com/TEYIcSu.png)

Este sencillo plugin permite generar dependencia entre 2 &lt;select&gt; y entre ellos mostrar la relación región/comuna que conforma la distribución geopolítica de la República de Chile.

##### [Demo](http://www.csslab.cl/ejemplos/geoRegionalizacion/demo.html)

### Dependencias:

[jQuery](http://jquery.com/)

### HTML base:

```html
<label>Región: </label>
<select id="region">
	<option value="">Seleccione</option>
</select>
<label>Comuna: </label>
<select id="comuna">
	<option value="">Seleccione</option>
</select>
```

### Uso base:

```javascript
$('#region').geoRegionalizacion({
	regionDependiente: '#comuna'
});
```

### Uso avanzado:

```javascript
$('#region-avanzado').geoRegionalizacion({
	regionDependiente: '#comuna-avanzado',
	onRegionSelect: function(){
		console.log($(this).val());
	},
	onComunaSelect: function() {
		console.log($(this).val());
	},
	onCreate: function(){
		$('#region-avanzado, #comuna-avanzado').selectric('refresh');
	}
});
```

### Licencia:
[MIT](https://github.com/juanbrujo/georegionalizacion/blob/master/LICENSE)
