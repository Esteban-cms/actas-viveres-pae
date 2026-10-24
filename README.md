# Actas de víveres – PAE

Aplicativo web estático (sin servidor) para generar las actas de entrega de víveres por sede.

## Publicar en GitHub Pages
1. Sube estos archivos (`index.html`, `data.js`, `README.md`) a un repositorio.
2. Settings → Pages → Branch `main` / carpeta `/root` → Save.
3. Abre la URL que te da GitHub. También funciona abriendo `index.html` directamente en el navegador.

## Uso
1. **Entrega**: operador, placa, fechas, ciclos y días (desmarca los días sin clase).
2. **Sedes y cupos**: edita, agrega o elimina sedes.
3. **Productos y empaques**: nombre, unidad, gramos por empaque y ★ para la lista del proveedor.
4. **Gramajes por menú**: gramos por cupo de cada producto en los menús 1 a 20.
5. **Generar**: PDF con todas las actas (carta), ZIP con un PDF por sede y lista del proveedor (frijol, carne de res, cerdo y huevo).

Los cambios se guardan en el navegador. Usa "Guardar configuración (.json)" para respaldarlos o llevarlos a otro equipo.
Los datos iniciales (`data.js`) vienen del archivo ACTA_DE_VIVERES_ACTUALIZADA; incluye los logos.
Cálculo: (suma de gramos por cupo de los días marcados × cupos) ÷ gramos por empaque, redondeado hacia arriba.
