# Actas de víveres – PAE

Aplicativo web estático (sin servidor) para generar las actas de entrega de víveres por sede.

## Publicar en GitHub Pages
1. Sube estos archivos (`index.html`, `data.js`, `README.md`) a un repositorio.
2. Settings → Pages → Branch `main` / carpeta `/root` → Save.
3. Abre la URL que te da GitHub. También funciona abriendo `index.html` directamente en el navegador.

## Uso
1. **Entrega**: operador, placa, fechas, semanas (1 y 2 = menús 1-10; 3 y 4 = menús 11-20) y días (desmarca los días sin clase).
2. **Sedes y cupos**: edita, agrega o elimina sedes.
3. **Generar**: PDF, ZIP y lista del proveedor.
4. ⚙ **Productos y empaques** (casi no cambia): nombre, unidad, gramos por empaque y ★ para la lista del proveedor.
5. ⚙ **Gramajes por menú** (casi no cambia): gramos por cupo de cada producto en los menús 1 a 20.

En Generar: PDF con todas las actas (carta), ZIP con un PDF por sede y lista del proveedor (frijol, carne de res, cerdo y huevo).

Los cambios se guardan en el navegador. Usa "Guardar configuración (.json)" para respaldarlos o llevarlos a otro equipo.
Los datos iniciales (`data.js`) vienen del archivo ACTA_DE_VIVERES_ACTUALIZADA; incluye los logos.
Cálculo: (suma de gramos por cupo de los días marcados × cupos) ÷ gramos por empaque, redondeado hacia arriba.
