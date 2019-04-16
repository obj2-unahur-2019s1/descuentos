# descuentos

Se solicita definir las siguientes  estructuras, interfaces: 

* Vuelo:
  - Monto por viajero.
  - Una posible retención del gobierno (monto) (se aplica sobre el total calculado).
  - Ganancia de despegar (monto variable).
  - Coeficiente por tipo de viajero (INFANT: 0.2, CHILD: 0.5, ADULT: 1).
  - Cantidad de viajeros.
  - Aerolínea
  - Origen
  - Destino
  - Descripción
  - Código proveedor
  - Descripción proveedor

* Hotel:
  - Cantidad de noches.
  - Precio por noche de una habitación.
  - Monto base por viajero.
  - Una posible retención del gobierno (monto) (se aplica sobre el total calculado).
  - Ganancia de despegar (monto variable).
  - Costo adicional por tipo de habitación (STANDAR: 0, DELUXE: 2000).
  - Cantidad de estrellas
  - Cantidad de habitaciones disponibles.
  - Descripción
  - Código proveedor
  - Descripción proveedor

* Ticket:
  - Límite máximo por día: 10000
  - Monto base por viajero.
  - Una posible retención del gobierno (monto)  (se aplica sobre el total calculado).
  - Ganancia de despegar (monto variable).
  - Precio adicional por tipo de viajero (INFANT: 200, CHILD: 900, ADULT: 1000).
  - cantidad de días.
  - Descripción
  - Código proveedor
  - Descripción proveedor
		
* Auto:
  - Cantidad de días.
  - Monto base.
  - Una posible retención del gobierno (monto) (se aplica sobre el total calculado).
  - Ganancia de despegar (monto variable).
  - Adicionales (gps, pantalla)
  - Categoría
  - Código proveedor
  - Descripción proveedor

## Requerimientos:

### Punto 1

- Calcular el total de un producto dado

- Calcular e informar descuento por promoción. Una promoción está expresada de la siguiente forma: 
  * Si el producto es un vuelo y el destino es ORL, aplicar un 20 % de descuento.
  * El hotel no tiene promociones.
  * Si el producto es un ticket y el monto total supera los 9000, aplicar un 10 % de des. 
  * Si el producto es un auto, incluye más de 2 adicionales y el proveedor es RENTA_CAR o DOLAR, aplicar un 5% de descuento.

### Punto 2
	 	 	
El equipo donde nos encontramos trabajando cuenta con un servicio de descuentos. Nos solicitan implementar una nueva versión, la cual calcule el descuento total a partir de un producto.

Tipos de descuento:
- Descuento por proveedor: se aplicará un 10% de descuento en caso de que el proveedor esa “H”.
- Descuento por total del producto: se aplicará un 5% si el monto total del producto supera los $10.000.

Contamos con la siguiente interface de servicio:

```
public interface DiscountService {
  BigDecimal getDiscount(Productproduct);
}
```

Implementar el servicio correspondiente, y las promociones adecuadas
