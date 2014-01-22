geoRegionalizacion
==================

Este sencillo plugin permite generar dependencia entre 2 &lt;select&gt; y entre ellos mostrar la relación region / comuna que conforma la distribución geopolítica de la República de Chile.

HTML base:
-------
	<label>Región: </label>
	<select id="region">
		<option value="">Seleccione</option>
	</select>
	<label>Comuna: </label>
	<select id="comuna">
		<option value="">Seleccione</option>
	</select>


Uso base:
-------
	$('#region').geoRegionalizacion({
   		regionDependiente: '#comuna',
   		onRegionSelect: function(){
      		console.log($(this).val());
   		},
   		onComunaSelect: function() {
      		console.log($(this).val());
   		}
	});

Uso avanzado:
-------
	$('#region-avanzado').geoRegionalizacion({
   		regionDependiente: '#comuna-avanzado',
   		onCreate: function(){
      		$('#region-avanzado, #comuna-avanzado').selectric('refresh');
   		}
	});


