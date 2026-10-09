# Fase1_Psicometria_OCEAN_BigFive_v1

## 1. Instrucciones para el evaluado
A continuación encontrará 50 afirmaciones sobre su forma de ser.
Indique qué tan de acuerdo está con cada una usando esta escala:

1 = Muy en desacuerdo
2 = En desacuerdo
3 = Neutral
4 = De acuerdo
5 = Muy de acuerdo

Responda con sinceridad. No hay respuestas correctas ni incorrectas.

---

## 2. Cuestionario (50 ítems)

### Apertura (Openness) — 10 ítems
1. Tengo una imaginación vívida
2. Me interesan las ideas abstractas
3. Soy una persona curiosa
4. Disfruto pensando en teorías complejas
5. Tengo dificultad para entender ideas abstractas (R)
6. No me interesan las discusiones filosóficas (R)
7. Prefiero lo conocido a lo novedoso (R)
8. Me aburren los temas culturales o artísticos (R)
9. No me gusta el arte (R)
10. Evito las discusiones intelectuales (R)

### Responsabilidad (Conscientiousness) — 10 ítems
11. Soy meticuloso en mi trabajo
12. Sigo un horario establecido
13. Cumplo mis promesas
14. Hago las cosas según lo planeado
15. Dejo mis pertenencias por cualquier lado (R)
16. Desordeno las cosas (R)
17. A menudo olvido devolver cosas (R)
18. Huyo de mis responsabilidades (R)
19. Pierdo tiempo (R)
20. Me cuesta comenzar las tareas (R)

### Extroversión (Extraversion) — 10 ítems
21. Soy el alma de la fiesta
22. Hablo con muchas personas diferentes en las fiestas
23. No me importa ser el centro de atención
24. Inicio conversaciones fácilmente
25. Prefiero estar solo (R)
26. Tengo poco que decir (R)
27. Hablo poco (R)
28. Me quedo en segundo plano (R)
29. No me gusta llamar la atención (R)
30. Soy callado en compañía de extraños (R)

### Amabilidad (Agreeableness) — 10 ítems
31. Me intereso por los demás
32. Simpatizo con los sentimientos de los demás
33. Tengo un corazón tierno
34. Me tomo tiempo para los demás
35. Insulto a la gente (R)
36. Me desintereso de los problemas de otros (R)
37. Me peleo con los demás (R)
38. Me gusta vengarme de los demás (R)
39. Trato mal a los demás (R)
40. No me interesan los problemas de los demás (R)

### Neuroticismo (Neuroticism) — 10 ítems
41. Me estreso fácilmente
42. Me preocupo por muchas cosas
43. Cambio de humor con frecuencia
44. Me irrito fácilmente
45. Estoy relajado la mayor parte del tiempo (R)
46. Rara vez me siento triste (R)
47. Rara vez me preocupo (R)
48. Me mantengo tranquilo bajo presión (R)
49. Me siento cómodo conmigo mismo (R)
50. Rara vez pierdo la compostura (R)

**(R) = ítem de puntuación inversa**

---

## 3. Sistema de puntuación

### Paso 1: Invertir los ítems (R)
Puntuación invertida = 6 − respuesta original.
Ejemplo: si respondió 2, se convierte en 4.

### Paso 2: Sumar por dimensión
Cada dimensión tiene 10 ítems. El rango bruto va de 10 a 50.

### Paso 3: Convertir a percentil
Usar una tabla de baremos. Ejemplo con muestra de referencia:

| Puntuación bruta | Percentil |
|---|---|
| 10–19 | 1–10 |
| 20–24 | 11–25 |
| 25–29 | 26–40 |
| 30–34 | 41–60 |
| 35–39 | 61–75 |
| 40–44 | 76–90 |
| 45–50 | 91–99 |

---

## 4. Prompt de extracción de rasgos

Eres un analista psicométrico. Recibirás:

Las respuestas crudas a 50 ítems del IPIP-50.

La tabla de percentiles de referencia.

Tu tarea:

Invertir los ítems marcados como (R) usando 6 − respuesta.

Sumar por dimensión (Apertura, Responsabilidad, Extroversión, Amabilidad, Neuroticismo).

Convertir cada suma a percentil usando la tabla.

Devolver un JSON con:
{
"Apertura": {"bruto": int, "percentil": int},
"Responsabilidad": {"bruto": int, "percentil": int},
"Extroversión": {"bruto": int, "percentil": int},
"Amabilidad": {"bruto": int, "percentil": int},
"Neuroticismo": {"bruto": int, "percentil": int}
}

No interpretes los resultados. Solo calcula.


---

## Advertencia importante

El IPIP-50 es de **dominio público**, pero los **baremos de percentiles** que uses deben declararse explícitamente:
- ¿De qué población vienen?
- ¿De qué estudio?
- ¿De qué año?

Sin esa fuente, la conversión a percentiles no es defendible. Puedes dejar la tabla como **provisional** y anotar que los baremos locales están pendientes (eso ya figura en `Brechas_Criticas!A2`).

---

## Siguiente paso

1. Copia todo eso en un archivo `.md`.
2. Súbelo a Google Drive, GitHub o Notion.
3. Copia la URL en `Auditoria_Cuadernos!N2`.
4. Cambia `C2` de `(Faltante)` a `Fase1_Psicometria_OCEAN_BigFive_v1`.
5. Actualiza `L2` si hace falta.

Cuando lo tengas subido, avísame y verificamos si `R2` cambia de estado.