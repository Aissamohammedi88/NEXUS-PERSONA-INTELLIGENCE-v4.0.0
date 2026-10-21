# NEXUS-PERSONA-INTELLIGENCE-v4.0.0
# Sources (10) : # Développeurs : GitHub, StackOverflow, PyPI, HackerNews # Académique : OpenAlex, Crossref, ArXiv # Général : DuckDuckGo, Wikipedia # Réseau Social : Reddit (via API publique) # ──────────────────────────────── # Robustesse : # - Circuit breaker par source (isolation des pannes) # - Retr
# 🕵️ NEXUS PERSONA INTELLIGENCE v4.0.0

> *Moteur de renseignement open source (OSINT). 10 sources. 0 LLM. 100% local.*

[![Version](https://img.shields.io/badge/version-4.0.0-00f3ff?style=for-the-badge)](#)
[![Python](https://img.shields.io/badge/Python-3.9%2B-3776AB?style=for-the-badge&logo=python&logoColor=white)](#)
[![OSINT](https://img.shields.io/badge/OSINT-Intelligence-ff00ea?style=for-the-badge)](#)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](#)

---

## 🧠 Le Concept

La plupart des outils d'OSINT (Open Source Intelligence) sont soit des scripts fragiles, soit des SaaS payants qui envoient vos requêtes dans le cloud. 

**Nexus Persona** est un moteur d'intelligence autonome écrit en Python pur (sans aucune dépendance externe, pas même `requests`). Il interroge 10 bases de données publiques en parallèle pour dresser le profil d'une personne ou d'une entité.

### Ce qui rend ce moteur unique :
1. **Zéro LLM** : La synthèse des résultats est faite par des algorithmes mathématiques (TF-IDF, TextRank, MMR), pas par OpenAI ou Anthropic.
2. **Résilience absolue** : Si une source tombe (ex: Reddit bloque), le *Circuit Breaker* l'isole, et le moteur continue avec les 9 autres.
3. **10 Sources OSINT** :
   - *Développeurs* : GitHub, StackOverflow, HackerNews
   - *Académique* : OpenAlex, Crossref, ArXiv
   - *Général* : Wikipedia, DuckDuckGo
   - *Réseaux Sociaux* : Reddit

---

## 🚀 Installation

Aucune dépendance à installer. Le code utilise uniquement la bibliothèque standard de Python (stdlib).

```bash
git clone https://github.com/Aissamohammedi88/nexus-persona-intelligence.git
cd nexus-persona-intelligence
python3 nexus_persona.py serve
