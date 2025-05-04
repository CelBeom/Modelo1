# Modelo 3D Simplificado desde Nube de Puntos

## Descripción
Este repositorio contiene un modelo 3D generado a partir de una nube de puntos proporcionada en la actividad “M2_T5_modelos”. El objetivo ha sido crear una malla triangulada, simplificada a menos de 10.000 vértices, parametrizada y texturizada, y publicarla en línea a través de GitHub.

## Herramientas utilizadas
- [MeshLab](https://www.meshlab.net/) — para todo el procesamiento 3D
- GitHub — para la publicación y compartición del modelo

## Pasos realizados

1. **Triangulación**  
   Se utilizó el filtro **Poisson Surface Reconstruction**. Se generaron normales previamente, ya que la nube original no las incluía. Se probó con diferentes profundidades y se eligió una profundidad final de 8 para lograr un equilibrio entre detalle y eficiencia.

2. **Simplificación**  
   Se aplicó el filtro **Quadric Edge Collapse Decimation**, reduciendo la malla original a menos de 10.000 vértices. Se preservaron los bordes y la topología durante el proceso.

3. **Parametrización**  
   Se utilizó el filtro **Parameterization: Voronoi Atlas** para generar las coordenadas UV, dividiendo la malla en parches listos para texturizar.

4. **Texturización**  
   Se generó una textura a partir del color por vértice de la nube original utilizando el filtro **Transfer Vertex Attribute to Texture**.

5. **Repositorio y Publicación**  
   Este repositorio contiene:
   - El modelo simplificado en formato `.obj`
   - La textura en formato `.png`
   - Este archivo `README.md` que documenta el proceso

## Archivos incluidos
- `modelo_simplificado.obj` — Malla final con UV
- `modelo_simplificado.mtl` — Materiales asociados
- `textura.png` — Textura generada desde el color por vértice
- `README.md` — Documentación del proceso

## Créditos
Actividad realizada como parte del curso de procesamiento de nubes de puntos y modelos 3D.
