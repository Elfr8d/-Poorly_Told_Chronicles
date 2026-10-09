---
layout: default
permalink: /
---

<div class="hero-stage">
  <div class="hero-title-wrapper">
    <img src="{{ '/assets/images/Crónicas urbanas en letras retro.png' | relative_url }}" alt="Crónicas Urbanas" class="hero-title-img">
  </div>
  <div class="deadlock-tape-badge">EL CÓDICE DEL CANON ABSOLUTO</div>
  <div class="hero-portraits-banner">
    <img src="{{ '/assets/images/header_portraits.webp' | relative_url }}" alt="Deadlock Heroes" class="hero-portraits-img">
  </div>
</div>

> *"A este espacio se le confiere la ineludible y excelsa prerrogativa de fungir como depositario arcano de nuestra exégesis colectiva. En sus entrañas inmateriales convergen las vicisitudes más trascendentales y los hitos inefables de nuestra cofradía, transmutando la vacuidad de lo efímero en un canon imperecedero. Constituye, en suma, el baluarte cronístico donde la arquitectura de nuestras vivencias elude el inexorable y ruinoso devenir del tiempo."*

---

## 🌌 La Línea Temporal Sagrada

A continuación, se despliega el paradigma cronológico de nuestra estirpe. Únicamente los eventos ratificados y exentos de refutación (aprobados mediante *Pull Request* hacia `Sagrada_linea_del_el_Tiempo`) ostentan el derecho de residir en este índice.

<div class="sacred-timeline">
{% assign eventos_cronologicos = site.pages | where_exp: "item", "item.estado == 'Canonizado'" | sort: "fecha" %}
{% for evento in eventos_cronologicos %}
  <div class="timeline-item">
    <div class="timeline-marker"></div>
    <div class="timeline-card">
      <div class="timeline-header">
        <span class="timeline-date">{{ evento.fecha }}</span>
        {% if evento.epoca %}<span class="timeline-epoch">{{ evento.epoca }}</span>{% endif %}
      </div>
      <h3 class="timeline-title">{{ evento.titulo }}</h3>
      {% if evento.descripcion %}<p class="timeline-desc">{{ evento.descripcion }}</p>{% endif %}
      <a href="{{ evento.url | relative_url }}" class="timeline-btn">📜 Abrir Crónica Completa →</a>
    </div>
  </div>
{% endfor %}
</div>

---

## ⚖️ El Protocolo de Canonización

¿Presenciaste un suceso histórico o deseas someter una memoria al juicio del Cónclave?

1. Consulta el manual oficial: [📜 Guía de Contribución](GUIA_CONTRIBUCION.md).
2. Clona el molde oficial: [📋 Plantilla de Eventos](eventos/_PLANTILLA_EVENTO.md).
3. Abre tu rama y somete tu *Pull Request* hacia la rama sagrada: **`Sagrada_linea_del_el_Tiempo`**.