+++
title = "Úkoly"
date = 2025-09-22
draft = false
+++

# Úkoly

Zde najdete všechny zadané úkoly v rámci předmětu **ZPC 2025 – Jak vyrobit téměř cokoliv**.

Každý úkol má samostatnou stránku s popisem postupu, použitými technologiemi a výsledky.

---

<style>
.ukoly-wrapper {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 1.2rem;
  margin-top: 2rem;
}

.ukol-card {
  background: #ffffff;
  border: 1px solid #e0e0e0;
  border-radius: 12px;
  padding: 1.2rem 1.5rem;
  box-shadow: 0 2px 5px rgba(0,0,0,0.05);
  transition: all 0.2s ease-in-out;
}

.ukol-card:hover {
  transform: translateY(-4px);
  box-shadow: 0 4px 12px rgba(0,0,0,0.15);
}

.ukol-card a {
  text-decoration: none;
  color: #007acc;
  font-weight: 600;
  font-size: 1.1rem;
}

.ukol-card a:hover {
  text-decoration: underline;
}

.ukol-card p {
  margin: 0.5rem 0 0;
  color: #444;
  font-size: 0.95rem;
}
</style>

<p><strong>TEST HTML</strong></p>

<div class="ukoly-wrapper">
  {{ range .RegularPagesRecursive.ByDate }}
  <div class="ukol-card">
    <a href="{{ .RelPermalink }}">{{ .Title }}</a>
    {{ with .Summary }}
      <p>{{ . }}</p>
    {{ end }}
  </div>
  {{ end }}
</div>