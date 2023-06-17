# Lenguaje de programación Javhan
Este lenguaje de programación esta diseñado para mejorar las experiencias de los usuarios
a la hora de manejar datos, hay distintos lenguajes de programación con distintos metodos
de almacenar, obtener, crear y destruir datos.

En javascript tenemos el JSON, esta herramienta nos sirve de mucho, porque esta es capaz de
hacer Objetos que, no necesariamente tienen que seguir una regla en especifico,
como en java, en cambio, en java tenemos que crear clases y si necesitamos 80 objetos
tendríamos que crear una clase para cada uno, cada lenguaje tiene sus ventajas y sus
desventajas.

**Javascript:**
| PROS                                                                           | CONTRAS                                                                   |
| ------------------------------------------------------------------------------ | ------------------------------------------------------------------------- |
| Facil manejo de datos con fetch y otras cosas como, array de funciones, etc... | Muchos errores de conversion de tipos                                     |
|                                                                                | El json tiene una estructura de datos no clara, eso puede generar errores |

**Java:**
| PROS 																																																																																																																			| CONTRAS																																								 |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Tiene variadas clases que permiten que casi no haya errores de conversion de tipos, y normalmente resulta de más comodidad para principiantes. Y esto porque en javascript si creo una funcion y le pongo un argumento, espero que el que llame a esa funcion me entrege ese valor, pero como es de variable múltiple, tambien me puede entregar otro valor. Provocando un inevitable error de tipos. 																		| Si quieres obtener muchos tipos de datos, deberías crear una clase para cada uno, lo cual es muy aburrido y probablemente te tardes más, pero siempre hay alternativas |
| En java, tenemos un remplazo más viable al json, pero que sigue siendo un poco peligroso, este remplazo es la función HashMap que permite guardar muchos valores como en json, hasta tenemos la función `toString()` que esta nos permite convertir todo el contenido a un String, pero si un valor no está definido, me devolverá como respuesta, null, o sea el valor no existe, pero podemos crear una excepción que explique todo para que el usuario pueda solucionarlo. |																																										 |

Que bueno que en Javhan hay muchas alternativas.

	#module name='MiModulo1'
	#include 'jah.funcs.Asynchronic'
	
	// Creamos un objeto con un metodo
	Mapper<String, Object> json = new Mapper<String, Object>();

	// Definimos funciones y variables
	@private json.value = true;

	json.isTrue => bool() {
		return value;
	}
	json.isFalse => bool() {
		return !value;
	}

	@Asynchronic
	public void LeerJson(Mapper<String, Object> json)
	{
		// Creamos una excepcion si el valor no contiene nada
		Exception !json.minimalRules(Boolean isTrue, Boolean isFalse), NullPointerException.class;
		if (json.isTrue()) {
			// Vamos a hacer una petición
			HttpRequest request = new HttpRequest();
			request.setMode("GET");

			// ERROR: Esta petición es asincronica asi que hay que convertir todo en asincronico.
			// Pero hay una solucion, con Asynchronic.await podemos hacer eso
			// Ya lo hicimos pero sigue habiendo un error

			return @await request.make(@Port 5566, @Ip 'https://www.google.com/');
			
		}

	}
	