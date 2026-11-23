# Actas de víveres – PAE 2027 (Primaria y Secundaria)

Página web que funciona sin servidor y sin internet. Genera las actas de entrega de víveres por sede, la lista del proveedor y el pedido consolidado con las dos minutas del ciclo de menús 2027:

- **Primaria**: preescolar (prejardín, jardín y transición) y 1° a 5°.
- **Secundaria**: 6° a 11° (secundaria y media).

## Archivos
- `index.html`: el aplicativo.
- `data.js`: logos, catálogo de productos, gramajes de los 20 menús para los dos niveles, y sedes.
- `pdf-lib.min.js`: librería para crear los PDF. Va incluida para que funcione sin internet.

## Publicar en GitHub Pages
1. Suba los cuatro archivos a un repositorio.
2. Vaya a Settings → Pages → Branch `main` / carpeta `/root` → Save.

También funciona abriendo `index.html` directamente en el navegador, con los tres archivos en la misma carpeta.

## Uso
1. **Entrega y días**: datos de la entrega, fecha de entrega y días con clase. El consumo empieza el siguiente día hábil y se saltan los festivos de Colombia.
2. **Sedes y cupos**: cupos de primaria y secundaria de cada sede. Hay tres formas de llenarlos:
   - escribir los totales;
   - abrir **Por grados** y escribir la matrícula de cada grado;
   - usar **Pegar cupos desde Excel**, ya sea con 3 columnas (DANE o nombre, primaria, secundaria) o con 15 columnas (DANE o nombre y los 14 grados).
3. **Revisar y generar**: muestra una lista de revisión y la vista previa del acta. Desde ahí se descarga el PDF con todas las actas, el ZIP con un PDF por sede, la lista del proveedor con el pedido, y el pedido en CSV para Excel.
4. **Productos y empaques** (configuración): unidad, gramos por empaque y ★ para la lista del proveedor. La etiqueta "Por confirmar" marca los empaques asignados por defecto.
5. **Gramajes por menú** (configuración): peso bruto por cupo de los 20 menús, en una pestaña para primaria y otra para secundaria.

## Cálculo
Para cada sede y producto:
`⌈ (g primaria de los días marcados × cupos primaria + g secundaria × cupos secundaria) ÷ gramos por empaque ⌉`

- Se usa el **peso bruto** de la minuta, que es lo que se compra.
- El agua no se cuenta.
- El huevo se cuenta por unidades de 50 g.
- Los productos a granel (gramos por empaque = 1) se muestran en kg.

Los cambios se guardan en el navegador. Use **Guardar copia (.json)** para respaldarlos o llevarlos a otro equipo. Si en el mismo navegador estaba la versión anterior, la entrega y las sedes se traen solas, con todos los cupos en primaria.
