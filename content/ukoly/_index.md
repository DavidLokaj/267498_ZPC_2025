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
.ukol-list {
  display: flex;
  flex-direction: column;
  gap: 10px;
  margin-top: 20px;
}
.ukol-card {
  padding: 12px 16px;
  background-color: #f4f4f4;
  border-left: 4px solid #007acc;
  border-radius: 6px;
  transition: background-color 0.2s ease;
}
.ukol-card:hover {
  background-color: #e8f2ff;
}
.ukol-card a {
  text-decoration: none;
  color: #000;
  font-weight: 500;
}
</style>

<div class="ukol-list">
  {{ range .RegularPagesRecursive.ByDate }}
  <div class="ukol-card">
    <a href="{{ .RelPermalink }}">{{ .Title }}</a>
  </div>
  {{ end }}
</div>

{{ range .RegularPagesRecursive.ByDate }}
- [{{ .Title }}]({{ .RelPermalink }})
{{ end }}