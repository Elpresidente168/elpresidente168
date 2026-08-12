# La Carrera Política v7 — Simulador Político Uruguayo

> ¿Podés llegar de militante de Cordón a Presidente de la República? De Salto a Torre Ejecutiva. Un simulador narrativo de la política uruguaya donde casi nadie llega, y perder también cuenta historia.

**Demo en vivo:** https://elpresidente168.github.io/elpresidente168/

![banner](https://elpresidente168.github.io/elpresidente168/banner.jpg)

### Qué es

**La Carrera Política** es un juego narrativo web, gratuito, sin login. Empezás con 24 años en 2028 y tenés que construir tu carrera: Junta Departamental, Diputado, Senado, Intendencia y, si la pegás, Presidencia.

No es un juego de ganar siempre. El 80% de las partidas terminan como *el Diputado Eterno, el Intendente Histórico o el Presidente del Partido que nunca llegó*. Llegar a Presidente es 1 de cada 15 partidas. Como en la vida real.

### Novedades v7 (vs v6)

- **Onboarding minimal:** Solo nombre + partido. 2 clics y estás jugando.
- **Origen importa:** Elegís Montevideo (Cordón, Pocitos, Cerro, Casavalle) o Interior (Salto, Paysandú, Tacuarembó, Maldonado, Rocha, Canelones). Cambia diálogos, bonus y eventos.
- **HUD limpio:** Chau 5 tabs de encuestas/país/rivales. Solo 3 barras: Popularidad / Reputación / Estabilidad + último titular.
- **Motor anti-repetición:** 54+ eventos con tags por origen/edad/partido. No se repiten hasta vaciar el mazo. Podés jugar 20 veces sin ver lo mismo.
- **Se puede perder (y está bueno):** 9 finales distintos, desde Presidente hasta consultor en Paraguay.
- **Pausa narrativa:** Cada elección ahora queda fija con pantalla de consecuencia + botón Continuar (pedido v7.1).
- **SEO real:** Landing con texto indexable, JSON-LD VideoGame, sitemap, OG dinámico para compartir final en WhatsApp.

### Cómo se juega

1.  Elegí tu nombre y partido (FA, PN, PC, Independiente)
2.  Elegí de dónde venís. Eso te da buffs: Interior + popularidad territorial, MVD + recursos/prestigio.
3.  Cada decisión sube/baja Popularidad, Reputación, Estabilidad y Escándalos.
4.  Elecciones clave:
    - 27 años: Junta Departamental / Edil
    - 32 años: Diputado
    - 38 años: Senado
    - 44 años: Intendencia
    - 50 años: Presidencia (necesitás 45% + balotaje)
5.  Si tu Estabilidad < 5 o Escándalos > 95, caés.

### Finales

- **Presidente de la República** (legendario)
- **Senador**
- **Intendente Histórico de [tu depto]**
- **Diputado Eterno**
- **Presidente del Partido / Dueño de la lapicera**
- **El Operador** (poder en las sombras)
- **El que se fue a la chacra** (retiro digno)
- **Consultor / Embajador**
- **El caído por escándalo**

Cada final genera una tapa tipo Búsqueda con tu CV, legado (0-100) y titulares.

### Stack técnico

- React (single file component, sin build step para GitHub Pages)
- Tailwind CSS vía CDN (clases utilitarias)
- 100% client-side, sin backend
- `localStorage` para partidas guardadas (`carreraPolitica_v7`)
- Listo para deploy estático

### Correr local

No necesitas nada:

```bash
# Clonar
git clone https://github.com/elpresidente168/elpresidente168.git
cd elpresidente168

# Abrir index.html en el browser, o servir con:
python -m http.server 8000
# o
npx serve .
```

El juego es un solo `index.html` + assets.

### Deploy

El repo ya está configurado para GitHub Pages desde `main` / `docs` o root.

1.  Push a `main`
2.  Settings > Pages > Source: main / root
3.  Tu juego queda en `https://elpresidente168.github.io/elpresidente168/`

No olvides actualizar:
- `sitemap.xml` con la fecha
- `banner.jpg` (1200x630) para OG
- `robots.txt`

### SEO Checklist (ya implementado en v7)

- [x] Title: `La Carrera Política - Simulador para ser Presidente de Uruguay`
- [x] Description 155 chars
- [x] H1/H2 con texto real indexable (no solo canvas)
- [x] JSON-LD VideoGame
- [x] Open Graph + Twitter Card con imagen
- [x] OG dinámico por final (para viralizar en WhatsApp)
- [x] sitemap.xml + robots.txt
- [x] Core Web Vitals < 2.5s (bundle <150kb)
- [x] FAQ schema

Keywords objetivo: `simulador político uruguayo, juego presidente uruguay, juego política uruguaya, simulador frente amplio`

### Roadmap v7.1 / v8

- [ ] Pausa con botón Continuar en cada consecuencia (pedido)
- [ ] 150 eventos (ahora 54) con variantes por departamento
- [ ] Internas partidarias jugables
- [ ] Debates TV con mini-juego
- [ ] Sistema de financiamiento / casos judiciales
- [ ] Multiplayer: comparar legado con amigos
- [ ] Sonidos: candombe suave + bocina de ómnibus

### Créditos

Idea, código y rosca por [@m.alvcig](https://www.instagram.com/m.alvcig) - Miguel Alves.
Hecho con mate, facturas y sufrimiento electoral uruguayo.

Inspirado en *The Political Machine*, *Reigns* y las internas del Frente Amplio a las 2am en Cordón.

### Licencia

MIT - Hacé lo que quieras, pero si llegás a Presidente avisá.

---

¿Jugaste? Contame en qué terminaste. La mayoría termina como Diputado Eterno, y está perfecto.
