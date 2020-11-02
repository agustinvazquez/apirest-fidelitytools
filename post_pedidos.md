POST_PEDIDOS

### URL 
https://apirest.fidelitytools.net/api/Pedidos?xKey=

### HTTP METHOD
POST

### PARAMETROS
##### Headers
Content-Type: "application/json"

##### Body
Datos minimos necesarios
```JSON
{
    "persona": {
        "sitio": {
            "idSitio": 266
        },
        "habilitado":"S",
        "segmento": {
            "idSegmento": 4551
        },
        "nombre":"JHON",
        "apellido": "DOE",
        "email":"JHONDOE@fidelitytools.com"
    },
    "tipoContenido": {
        "idTipoContenido": 3565
    },
    "sitio": {
        "idSitio": 266
    },
    "formaPago": "Sol",
    "listaProductosxPedido": [
        {
            "producto": {
                "idProducto": 161466,
                "titulo": "NOMBRE PROD."
            },
            "cantidad": 1,
            "precio": 10000,
            "subTotal": "10000"
        }
    ],
    "total": "10000"
}
```

Pedido completo

```JSON
{
    "idPedido":12342314,
    "fecha":"31/10/2020",
    "estado":"Pendiente",
    "estadoPago": {"idEstado": 7},
    "destino":"DESTINO 123, DESTINO",
    "entrega":"ENTREGA 123, ENTREGA",
    "transporteNombre":"NOMBRE TRANSPORTE",
    "transpoorteCosto":777.11,
    //Si completamos el codigo descuento el descuento que se aplicara sera el valor enviado dentro del campo "descuento", en este caso el codigo "CODIGO_123" equivale a 1000.11
    "codigoDescuento":"CODIGO_123",
    "descuento": 1000.11,
    "logPedido": "Alta de pedido por sitio web",
    "observaciones":"observaciones",
    "observacionesPedido": [
        {
            "nombreCampo": "clave",
            "valor":"valor"
        },
        {
            "nombreCampo": "clave1",
            "valor":"valor1"
        }
    ],
    "persona": {
        "sitio": {
            "idSitio": 266
        },
        "habilitado":"S",
        "segmento": {
            "idSegmento": 4551
        },
        "nombre":"JHON",
        "apellido": "DOE",
        "empresa": "JHON COMPANY",
        "email":"JHONDOE@fidelitytools.com",
        "dni":1231234,
        "pref3":351,//movil
        "movil":77888999,
        "pref1":3543, //telefono
        "telefono":444555,
        "direccion":"Calle 123",
        "numero":"123",
        "piso":"123",
        "dpto":"123",
        "provincia": "Cordoba",
        "cp":5107,
        "observaciones":"observaciones - persona"
        //Perfiles Generales
        "perfilCustomxPersona": [
            {
                "idPerfil": 123, //idPerfil general
                //Valores
                "perfilesCustomValor": [
                    {
                        "idPerfilCustomValor": 123
                    }
                ]
            }
        ],
        //Campos personales
        "datosDurosxSitioxPersona": [
            {
                "idDatoDuro":123,
                "valor":"valor"
            }
        ]
    },
    "tipoContenido": {
        "idTipoContenido": 3565
    },
    "sitio": {
        "idSitio": 266
    },
    "formaPago": "Sol",
    "listaProductosxPedido": [
        {
            "producto": {
                "idProducto": 161466,
                "titulo": "NOMBRE PROD."
            },
            "cantidad": 1,
            "precio": 10000,
            "subTotal": "10000"
        }
    ],
    "total": "10000"
}
```

Estado Pago
- ID:1 - El pago fue aprobado y acreditado.
- ID:2 - El pago se encuentra pendiente de acreditación
- ID:3 - El pago está siendo revisado
- ID:4 - El pago fue rechazado. El usuario puede intentar nuevamente.
- ID:5 - El pago fue devuelto al usuario.
- ID:6 - El pago fue cancelado por superar el tiempo necesario para realizar el pago o por una de las partes.
- ID:7 - Se inició una disputa para el pago.
- ID:12 - Sin Definir
- ID:19 - Fue hecho un contracargo en la tarjeta del pagador.
- ID:20 - El pago ha sido autorizado pero aún no fue capturado.
- ID:21 - Presupuesto


