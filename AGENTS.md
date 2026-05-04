# AGENTS.md

## Proposito

Este repositorio organiza material de TSSL para estudio, consulta rapida y produccion de notas propias.
La estructura prioriza:

- busqueda rapida por tipo de material
- nombres estables y semanticos
- minima duplicacion
- compatibilidad con flujos agent-first

## Mapa rapido

- `00-inbox/`: entrada temporal para archivos nuevos todavia no curados
- `01-cursada-actual/`: material principal de la cursada vigente
- `02-parciales/`: parciales limpios, simulacros y fotos crudas
- `03-bibliografia/`: libros base y complementarios
- `04-tablas-y-formularios/`: tablas de consulta rapida
- `05-cursadas-anteriores/`: material historico util
- `06-notas-codex/`: notas y resumentes generados en chat
- `07-archivo-original/`: zips originales y variantes duplicadas que se preservan por referencia
- `docs/`: indice, convenciones y notas de curacion

## Reglas de organizacion

- No dejar PDFs sueltos en la raiz.
- Todo archivo nuevo entra primero en `00-inbox/` si todavia no esta claro donde va.
- Si el destino ya existe y el archivo es identico, conservar una sola copia util.
- Si hay dos variantes parecidas pero no identicas, dejar una principal y mover la otra a `07-archivo-original/variantes-duplicadas/`.
- Las clases manuscritas van en `01-cursada-actual/04-clases-tablet/clase-XX/`.
- Las notas propias o generadas con Codex van en `06-notas-codex/` y deben ser `.md`.
- Las fotos crudas de parciales no se renombran masivamente sin revisar contexto; quedan en `02-parciales/90-fotos-crudas/`.

## Convencion de nombres

Usar minusculas y guiones:

- `teorico-NN-tema-fuente.pdf`
- `practico-NN-tema-fuente.pdf`
- `parcial-0N-anio-variante.pdf`
- `clase-0N-tipo-tablet-AAAA-MM-DD.pdf`
- `libro-autor-titulo.pdf`
- `tabla-tema.pdf`
- `nota-codex-tema.md`

Evitar:

- sufijos como `(1)`, `(2)`, `final`, `nuevo`, `copy`
- nombres genericos como `capitulo3.pdf` si el archivo en realidad es una guia practica

## Flujo esperado para agentes

1. Identificar tipo de material.
2. Revisar si ya existe una copia o una version mas nueva.
3. Revisar el contenido del PDF si el nombre es ambiguo.
4. Mover al directorio correcto.
5. Renombrar con la convencion.
6. Actualizar `docs/indice-material.md` si cambia el inventario relevante.
7. Registrar excepciones o dudas en `docs/observaciones-de-curacion.md`.

## Dudas conocidas de este repo

- Los archivos `Capitulo*_Oppenheim...` de la cursada actual no son capitulos del libro: son practicos basados en ejercicios de esos capitulos.
- Existe al menos un archivo de parcial cuyo nombre original no coincide del todo con el encabezado interno; se preservo una marca de cautela en su nombre.
- Hay material historico muy valioso en `05-cursadas-anteriores/`, pero no debe mezclarse con la cursada actual salvo que se curen equivalencias de tema.
