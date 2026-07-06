# 🤖 SEC Supply Chain Analyst Agent

Un agent d'intelligence économique de niveau production conçu pour parser les rapports financiers de la SEC (**Form 10-K**) et isoler chirurgicalement les goulots d'étranglement logistiques, technologiques et géopolitiques (les signaux faibles souvent noyés dans la langue de bois d'entreprise).

---

## 🎯 Valeur Ajoutée & Architecture
L'architecture a été pensée pour contourner les restrictions et le bruit des documents financiers :
* **Extraction ciblée :** Isolation automatique des sections `Item 1A (Risk Factors)` et `Item 7 (MD&A)` pour économiser 85% de tokens.
* **Production-Ready :** Gestion du rate limiting de l'API Anthropic (backoff exponentiel) et respect strict de la politique de requêtes de la SEC (User-Agent requis sous peine de code 403).
* **Fallback Dynamique :** Si la structure HTML du 10-K dévie des standards, l'agent bascule sur un mode de capture globale défensive pour éviter le crash.

---

## 📦 Installation & Lancement

1. Cloner le projet :
\`\`\`bash
git clone https://github.com/VOTRE_PSEUDO/sec-ai-supplychain-analyst.git
cd sec-ai-supplychain-analyst
\`\`\`

2. Installer les dépendances :
\`\`\`bash
pip install -r requirements.txt
\`\`\`

3. Configurer le fichier `.env` à la racine :
\`\`\`env
ANTHROPIC_API_KEY=sk-ant-api03-XXXXXXXXXXXXXXXXXXXXX
SEC_USER_AGENT="FinTechPortfolioAgent/1.0 (votre_email@domaine.com)"
\`\`\`

4. Lancer l'analyse :
\`\`\`bash
python sec_analyst_agent.py
\`\`\`

---

## 📊 Exemple de Rapport Généré (Extrait sur NVIDIA - NVDA)

🎯 **Résumé Exécutif des Risques Subis**
Dépendance extrême à un écosystème ultra-centralisé de fonderies et de packaging avancé pour les puces d'accélération IA.

⚠️ **Goulots d'Étranglement Technologiques Majeurs**
* Dépendance exclusive aux architectures de fonderie externes. Risque majeur sur la propriété intellectuelle en cas de rupture de licence ou de blocage d'accès aux technologies de lithographie de pointe (EUV).

⛓️ **Goulots d'Étranglement Logistiques & Supply Chain**
* **Le point de rupture unique (Single Point of Failure) :** Dépendance critique envers TSMC pour la fabrication des puces et les technologies de packaging avancé **CoWoS** (Chip-on-Wafer-on-Substrate). Capacité de production mondiale sous tension maximale.

📊 **Niveau de Risque Global**
* **Score : 4/5** -> Risque géopolitique (Taïwan) et technique maximal, atténué uniquement par le pouvoir de pricing de l'entreprise sur ses clients.

---
### 🔍 Et si on devait le faire manuellement ? (Méthodologie d'Audit)
Si vous ne voulez pas passer par l'automatisation, voici la procédure "chirurgicale" pour extraire ces informations directement à la source :

1. **Accès EDGAR** : Rendez-vous sur le site officiel de la SEC (Edgar Company Search).
2. **Recherche de Ticker** : Tapez le symbole de l'entreprise (ex: NVDA).
3. **Filtrage** : Filtrez les résultats pour ne garder que les formulaires **10-K** (le rapport annuel).
4. **Audit de l'Item 1A** : Ouvrez le rapport HTML et cherchez la section **"Item 1A. Risk Factors"**.
5. **Analyse de contenu** : Scannez les paragraphes traitant du "Manufacturing" et des "Suppliers". C'est ici que l'entreprise est légalement contrainte de divulguer ses vulnérabilités critiques (ex: dépendance TSMC, CoWoS).

*Pourquoi c'est important ?* : L'automatisation est une question de vitesse, mais la compréhension manuelle est une question de maîtrise. Ne faites jamais confiance à une analyse IA sans avoir vérifié la section "Risk Factors" à la source.
---
